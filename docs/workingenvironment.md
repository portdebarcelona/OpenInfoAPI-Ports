# Working environment
To work in this project we have chosen and setup a set of tools. Here we explain which tools we use. Each decision is a balance between functionalities and ease of use. Questions like:
- Editor
- Repository of code
- Web site
- Editor of OAS

Also, we consider aspects such as:
- Best practices to define APIs
- API-Led connectivity

## API Led Connectivity
Main goal is publish info that has meaning to humans. For that reason we'll try to follow guidelines of API led connectivity, centered in **Experience APIs**:
- https://blogs.mulesoft.com/learn-apis/api-led-connectivity/what-is-api-led-connectivity/

## Best Practices to define APIs
## Markdown extension
Better tools for editing markdown: https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one

## Open API editor
Main goal is define and publish webservices wiht OAS3.x specification. We chose [Open API (swagger) extension](https://marketplace.visualstudio.com/items?itemName=42Crunch.vscode-openapi).

We can need other tools: [Open API tools](https://openapi.tools/)

## Definition of APIs following OAS 3.x
Definition of APIs will follow [Open API Specification 3.x](https://github.com/OAI/OpenAPI-Specification). We evaluated [RAML](https://raml.org/) proposition, but OAS3 nowadays is outstanding. [review at](https://nordicapis.com/oas-vs-raml-whats-the-difference/)

## Web pages of project
Because github.com facilitates Gitpages processes with Jekyll.

## Blueprint for APIs
It's needed to expose APIs in web format to facilitate comprehension of API definisitons, as swagger do. We evaluate several options and choose
(Redoc)[https://github.com/Redocly/redoc] because is a very light way to publish Open API 3.0 directly from definition (yaml or json). Other products and services evaluated were:
- [Swagger-UI](https://swagger.io/tools/swagger-ui/)
- [APIDOC](https://apidocjs.com/). Preprocessing comments of programming code.
- [ReadME](https://readme.com/documentation)
- 
## Name of Code repository
**OpenInfoAPI-Ports**, then https://github.com/portdebarcelona/OpenInfoAPI-Ports. In a initial phase is under domain 'portofbarcelona'. In a future we will see.

## Code repository
Because our company (portofbarcelona) uses **Github.com**, this will be our code and documentation repository.

## Editor
**VSCode**: Visual Studio Code Editor is an outstanding editor that has many plugins and connection with git repositories
