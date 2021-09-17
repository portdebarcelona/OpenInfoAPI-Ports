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
  