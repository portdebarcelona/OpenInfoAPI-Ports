# Standardization Recommendations and Decisions

This document sumarizes all the decisions addopted during this project with the objective to develop a set of recommendations and best practices for the API definition.
   
## Open API version 3
- While we have chosen Open API version 3. 
- Advantages and disadvantages.

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

 