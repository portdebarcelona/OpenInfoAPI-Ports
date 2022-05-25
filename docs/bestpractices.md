# Best practices
# Recommendations 

This document summarizes all the decisions adopted during this project to develop a set of recommendations and best practices for the API definition.
   
## Keywords
- In this documment, the keywords to indicate requirement levels are to be interpreted as described in the Best Current Practice 14 (BCP 14) RFC2119 when, and only when, they appear in all capitals (RFC8174), as shown here:
  - "MUST", "REQUIRED" or "SHALL" mean that the definition is an absolute requirement of the specification.
  - "MUST NOT" or "SHALL NOT" mean that the definition is an absolute prohibition of the specification
  - "SHOULD" or "RECOMMENDED", mean that there may exist valid reasons in particular circumstances to ignore a particular item, but the full implications must be understood and carefully weighed before choosing a different course.
  - "SHOULD NOT" or "NOT RECOMMENDED", mean that there may exist valid reasons in particular circumstances when the particular behavior is acceptable or even useful, but the full implications should be understood and the case carefully weighed before implementing any behavior described with this label.
  - "MAY" or "OPTIONAL", mean that an item is truly optional. 


## Open API Specification (OAS)
- OAS is a framework for describing an API using a common language that everyone can understand. It is a specification independent of the programming language.
- There are other available frameworks, such as Summation, RAML and APIBlueprint but OAS helps to create clear docummentation, it is human and machine readable, it is easy to understand for programmers and non-programmers, and it is easy to make changes and test them.
- `Open API Specification` SHOULD be the framework to design our APIs.
    

## API versioning
- Open API provides a way to inform Version API 
- SHOULD be `version 3.0` or higher.

## Top-down approach
- To make the code clearer, we SHOULD think about the API before writing the code. 
- It is RECOMMENDED to design the API before writting any code.

## YAML
- OpenAPI definitions can be written in JSON or YAML. 
- `YAML` is RECOMMENDED, because it is easier to read and write. 

## JSON
- JSON (JavaScrip Object Notation) SHOULD be the format for accepting and responding API requests. It is NOT RECOMMENDED to use HTML or XML. 

## Use nouns instead of verbs in endpoints
- Because HTTP methods such as GET, POST, PUT, PATCH or DELETE are verbs for performing basic CRUD operations (Create with POST/PUT, read with GET, update with PUT/POST/PATCH and delete with DELETE), in the endpoints paths it is RECOMMENDED to use nouns, signifying what the endpoint does.

## Grouping Operations With Tags (from [OpenAPI specification](https://swagger.io/docs/specification/grouping-operations-with-tags/))
- We SHOULD group operations with `tags.` 

## Parameters
### Parameter Serialization (from [OpenAPI specification](https://swagger.io/docs/specification/serialization/))
- Serialization means translating data structures or object states into a format that can be transmitted and reconstructed later. OpenAPI 3.0 supports arrays and objects in operation parameters (path, **query**, header, and cookie) and lets you specify how these parameters should be serialized. 
- The serialization method is defined by the **style** and **explode** keywords:
style defines how multiple values are delimited. 
  - Possible styles depend on the parameter location – path, query, header or cookie.
  - explode (true/false) specifies whether arrays and objects should generate separate parameters for each array item or object property.

- `Query Parameters`
  - Query parameters support different style values and the following combination is RECOMMENDED:
    - form – (default) ampersand-separated values, also known as form-style query expansion. Corresponds to the {?param_name} URI template.

- The default serialization method is `style: form` and `explode: true`, and this is the combination is RECOMMENDED
- Some examples of the RECOMMENDED combination:
  - style: form 
  - explode: true
  -	If the URI template in these examples is: /users{?id}, then: 
    - The `primitive` value id = 5 is translated as: /users?id=5
    -	The `array` id = [3, 4, 5] is translated as: /users?id=3&id=4&id=5	
    -	The `object` id = {"role": "admin", "firstName": "Alex"} is translated as: /users?id=role=admin&firstName=Alex


## Request body (from [OpenAPI specification](https://swagger.io/docs/specification/describing-request-body/))
- With “create” and “update” operations (POST, PUT, PATCH) it is RECOMMENDED to use `request bodies`. For example, when creating a resource using POST or PUT, the request body usually contains the representation of the resource to be created.
- It is RECOMMENDED to use JSON for POST, PUT and PATCH request bodies
- When updating a record on a database, the parameters will be used to identify the record whereas the message body will provide its new content. 

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
  - A first step, the subscription/unsubscription `request` and
  - a second step, the subscription/unsubscription `validation`.
- After the first request, a validation key will be received and it should be incorporated as a parameter into the validation step.



# To do list


- Security Scheme
- Filtering
- Sorting
- Pagination of the results
- Application Rate Limiting
- Callbacks (from [OpenAPI specification](https://swagger.io/docs/specification/callbacks/))
-  Marketplace design




# Some other references
Here some places where give ideas about best practices defining APIS:
- https://github.com/RestCheatSheet/api-cheat-sheet
- https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api
- https://docs.python-eve.org/en/stable/rest_api_for_humans.html
- **https://www.merixstudio.com/blog/best-practices-rest-api-development/**
- https://www.merixstudio.com/blog/api-documentation-few-tips-will-help-you-write-it-well/
- http://apistylebook.com/design/guidelines/google-api-design-guide#api-design
- https://cloud.google.com/apis/design


  