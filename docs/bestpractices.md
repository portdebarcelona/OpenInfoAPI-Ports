# Best practices
# Standardization, Recommendations and Decisions

This document summarizes all the decisions adopted during this project to develop a set of recommendations and best practices for the API definition.
   
## Keywords
- In this documment, the keywords to indicate requirement levels are to be interpreted as described in the Best Current Practice 14 (BCP 14) RFC2119 when, and only when, they appear in all capitals (RFC8174), as shown here:
  - "MUST", "REQUIRED" or "SHALL" mean that the definition is an absolute requirement of the specification.
  - "MUST NOT" or "SHALL NOT" mean that the definition is an absolute prohibition of the specification
  - "SHOULD" or "RECOMMENDED", mean that there may exist valid reasons in particular circumstances to ignore a particular item, but the full implications must be understood and carefully weighed before choosing a different course.
  - "SHOULD NOT" or "NOT RECOMMENDED", mean that there may exist valid reasons in particular circumstances when the particular behavior is acceptable or even useful, but the full implications should be understood and the case carefully weighed before implementing any behavior described with this label.
  - "MAY" or "OPTIONAL", mean that an item is truly optional. 



## Open API versioning
- SHOULD be `version 3.x`.
- While we have chosen Open API version 3. 
- Advantages and disadvantages.

## YAML
- OpenAPI definitions can be written in JSON or YAML. `YAML` is RECOMMENDED, because it is easier to read and write. 

## JSON
- JSON (JavaScrip Object Notation) SHOULD be the format for accepting and responding API requests. It is NOT RECOMMENDED to use HTML or XML. 

## Parameter Serialization (from [OpenAPI specification](https://swagger.io/docs/specification/serialization/))
- Serialization means translating data structures or object states into a format that can be transmitted and reconstructed later. OpenAPI 3.0 supports arrays and objects in operation parameters (path, **query**, header, and cookie) and lets you specify how these parameters should be serialized. 
- The serialization method is defined by the **style** and **explode** keywords:
style defines how multiple values are delimited. 
  - Possible styles depend on the parameter location – path, query, header or cookie.
  - explode (true/false) specifies whether arrays and objects should generate separate parameters for each array item or object property.

- Query Parameters
  - Query parameters support different style values and the following combination is RECOMMENDED:
    - form – (default) ampersand-separated values, also known as form-style query expansion. Corresponds to the {?param_name} URI template.

- Althoug the default serialization method is *style: form* and *explode: true*, the combination `style: form` and `explode: false` is RECOMMENDED
- Some examples:
  - style: form 
  - explode: false
  -	If the URI template in these examples is: /users{?id}, then: 
    - The primitive value id = 5 is translated as: /users?id=5
    -	The array id = [3, 4, 5] is translated as: /users?id=3,4,5	
    -	The object id = {"role": "admin", "firstName": "Alex"} is translated as: /users?id=role,admin,firstName,Alex

## Grouping Operations With Tags (from [OpenAPI specification](https://swagger.io/docs/specification/grouping-operations-with-tags/))
- We SHOULD group operations with `tags.` 

## Use nouns instead of verbs in endpoints
- Because HTTP methods such as GET, POST, PUT, PATCH or DELETE are verbs for performing basic CRUD operations (Create with POST/PUT, read with GET, update with PUT/POST/PATCH and delete with DELETE), in the endpoints paths it is RECOMMENDED to use nouns, signifying what the endpoint does.

## Responses
- SHOULD include data results, enveloped by object with the same name as the web service. E.g. `noticeCategories`, `shipArrivals`
- MAY include some metadata of the API call (`metadata`).
- SHOULD include information on the parameters (`queryParams`).
- In case of error, read below:

### Errors
- SHOULD include `error` section with these attributes:
  - `code`: HTML response status code
  - `messageCode`: Code error description
  - `message`: Error description
  - `timestamp`: timestamp of error occurrence
- MAY include the most precise code, from the list of HTML status codes, that identifies the error returned by a server on a client's request and will help users to know what is going on – whether the request is successful, or if it fails, or something else. 

## Data types
  - MAY reuse schema.org data types when possible.

### Entities and attributes
  - `Entities` represent a thing. Entities include a semantic type that describes the type of thing represented by the entity.
  - Some examples of entities are: Person, Company, Building, Ship, Container... 
  - The naming convention for entities SHOULD be `upper camel case` (initial uppercase letter). 
  - `Attributes` are properties of entities, where a property is a combination of an attribute and its value.
  - Attributes describe the current state of the entity they belong to.
  - The naming convention for attibutes MUST be `lower camel case` (initial lowercase letter), also known as dromedary case.  

### Language
- `English` SHOULD be the language to identify entities and attributes.  

### Collections
- Collections SHOULD be identified with plural nouns. E.g. `portGates` is a collection with several entities named `portGate`.  


## Subscription or unsubscription management
### Two steps 
- Subscriptions and unsubscriptions MAY be managed in two steps:
  - A first step, the subscription/unsubscription request and
  - a second step, the subscription/unsubscription validation.
- After the first request, a validation key will be received and it should be incorporated as a parameter into the validation step.


## Pagination





# To do






## Security Scheme Object
- Defines a security scheme that can be used by the operations. Supported schemes are:
  
  - HTTP authentication, 
  - an API key (either as a header, a cookie parameter or as a query parameter), 
  - OAuth2's common flows (implicit, password, client credentials and authorization code) as defined in RFC6749, and 
  - OpenID Connect Discovery.

- Fields required for the supported schemes:
  - Common fields
    - type
    - description
  - HTTP authentication
    - scheme ([values registered in the IANA Authentication Scheme registry](https://www.iana.org/assignments/http-authschemes/http-authschemes.xhtml)]
    - bearerFormat
  - API key 
    - name
    - in (valid values are: query, header or cookie)
  - oauth2
    - flows (supported values are:  implicit, password, clientCredentials, authorizationCode)
    - These are the configuration details for a supported OAuth Flow:
      - authorizationUrl string (oauth2 ("implicit", "authorizationCode")) REQUIRED
      - tokenUrl string (oauth2 ("password", "clientCredentials", "authorizationCode")) REQUIRED 
      - refreshUrl string (oauth2)
      - scopes Map[string, string] (oauth2) REQUIRED 
  - openIdConnect
    - openIdConnectUrl


## Callbacks (from [OpenAPI specification](https://swagger.io/docs/specification/callbacks/))
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

## Marketplace design






# Best practices in defining API

We need to stablish some rules in defining APIs. For this reason we have been inspired in preceding efforts. Being that this openapi will be based in Restful services where JSON will be the data format of communications, we have been looking for some standard or best practices. Really doesn't exist a standard, but every webservice have solved this questions the best he could. 

## Which requirements the JSON API must fullfil 

- Simple
- Use RESTful URLs and actions
- Provide a way to inform Version API
- Provide method for filtering
- Provide method for sorting
- Provide method for searching
- Provide a way to limit which fields are returned from the API
- HATEOAS isn't practical just yet
- Use JSON where possible, XML only if you have to
- Naming convention for fields: camelCase
- Consider using JSON for POST, PUT and PATCH request bodies
- Provide a way to paginate results
- Provide a way to autoload related resource representations
- Provide a way to override the HTTP method
- Provide useful response headers for rate limiting
- Provide a way to return errors
- Effectively use HTTP Status codes


## Decision adopted and motivation
We appreciate this attempt to define a [JSON:API](https://jsonapi.org/format/1.1/)  standard, and we will use:

- **https://jsonapi.org/format/1.1/**


### Other Inspiring places
Here some places where give ideas about best practices defining APIS:
- https://github.com/RestCheatSheet/api-cheat-sheet
- https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api
- https://github.com/darrin/yaras/blob/master/restful-standards.md
- https://docs.python-eve.org/en/stable/rest_api_for_humans.html
- **https://www.merixstudio.com/blog/best-practices-rest-api-development/**
- https://www.merixstudio.com/blog/api-documentation-few-tips-will-help-you-write-it-well/
- http://apistylebook.com/design/guidelines/google-api-design-guide#api-design
- https://cloud.google.com/apis/design
## Best practices applied in this project

We have undertaked a comparison between Api style guides. We have looked for a API no specific for a sector, whetherThese are guidelines applied in this project.

## API for requests

- Veure DSCA API design principles 1.0 (on concreta molt bé com s'han de fer els requests)
## API for responses

- Formats de JSON per respondre (veure jsonapi.org,la de Google )
- jsonapi.org https://www.youtube.com/watch?v=RSv-Yv3cgPg 
- https://www.youtube.com/watch?v=LLe7Fi-wM3Q
- https://discuss.jsonapi.org/t/pragmatic-design-with-json-api-at-fitbit/1143
  