# Standardization Recommendations and Decisions

This document sumarizes all the decisions addopted during this project with the objective to develop a set of recommendations and best practices for the API definition.
   
## camelcase
- Naming convention for fields: camelCase. 

## Open API version 3
- While we have chosen Open API version 3. 
- Advantages and disadvantages.

## YAML
- OpenAPI is 3.0. OpenAPI definitions can be written in JSON or YAML. We recommend YAML, because it is easier to read and write. 

## Parameter Serialization (from [OpenAPI specification](https://swagger.io/docs/specification/serialization/))
- Serialization means translating data structures or object state into a format that can be transmitted and reconstructed later. OpenAPI 3.0 supports arrays and objects in operation parameters (path, **query**, header, and cookie) and lets you specify how these parameters should be serialized. 
- The serialization method is defined by the **style** and **explode** keywords:
style defines how multiple values are delimited. 
  - Possible styles depend on the parameter location – path, query, header or cookie.
  - explode (true/false) specifies whether arrays and objects should generate separate parameters for each array item or object property.

- Query Parameters
  - Query parameters support different style values and WE RECOMMEND:
    - form – (default) ampersand-separated values, also known as form-style query expansion. Corresponds to the {?param_name} URI template.

- Althoug the default serialization method is *style: form* and *explode: true*, WE RECOMMEND *style: form* and *explode: false* 
- Some exemples:
  - style: form 
  - explode: false
  -	If the URI template in these exemples is: /users{?id}, then: 
    - The primitive value id = 5 is translated as: /users?id=5
    -	The array id = [3, 4, 5] is translated as: /users?id=3,4,5	
    -	The object id = {"role": "admin", "firstName": "Alex"} is translated as: /users?id=role,admin,firstName,Alex

## Grouping Operations With Tags (from [OpenAPI specification](https://swagger.io/docs/specification/grouping-operations-with-tags/))
- WE RECOMMEND to group operations with tags. 

## Callbacks
- A callback is an asynchronous, out-of-band, request that a service will send to some other service in response to certain events. 
- A typical example of a callback is subscription functionality – users subscribe to certain events of a service and receive a notification when this or that event occurs. For example, an e-shop can send a notification to the manager on each purchase. 
- These notifications will be “out-of-band”, that is, they will go through a connection other than the connection through which a visitor works, and they will be asynchronous, as they will be out of the regular request-response flow. 

      paths:
        /subscribe:
          description: Add a subscriber
          post:
            parameters:
              - name: callbackUrl
                in: query
                required: true
                schema:
                  type: string
                  format: uri
              - name: event
                in: query
                required: true
                schema:
                  type: string
            responses:
              '201':
                description: Added
                content:
                  application/json:
                    type: object
                    properties:
                      subscriberId: 
                        type: string
                        example: AAA-123-BBB-456                    
            links:  # Link the returned id with the unsubscribe operation
              unsubscribeOp:
                operationId: unsubscribeOperation
                    parameters: 
                      Id: $response.body#/subscriberId
            callbacks:
              myEvent:
                '{$request.query.callbackUrl}?event={$request.query.event}':
                  post:
                    requestBody:
                      content:
                        application/json:
                          example:
                            message: Some event
                    responses:
                      '200':
                        description: OK
                    
        /unsubscribe:
          post:
            operationId: unsubscribeOperation
            parameters:
              - name: Id
                in: query
                required: true
                schema:
                  type: string

## Responses must include information on the API called (with their parameters
)