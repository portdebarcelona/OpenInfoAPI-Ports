# Back Stage notes

## Some technical questions

https://github.com/OAI/OpenAPI-Specification

https://github.com/OAI/OpenAPI-Specification/blob/master/IMPLEMENTATIONS.md

- How to documment an API:
  - Ratings:
    - [https://nordicapis.com/5-examples-of-excellent-api-documentation/](https://nordicapis.com/5-examples-of-excellent-api-documentation/)
    - [https://www.altexsoft.com/blog/api-documentation/](https://www.altexsoft.com/blog/api-documentation/)
    - [https://geekflare.com/api-documentation-tools/](https://geekflare.com/api-documentation-tools/)
  - Best practices:
    - https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api
    - https://github.com/darrin/yaras/blob/master/restful-standards.md
    - https://docs.python-eve.org/en/stable/rest_api_for_humans.html ( and https://docs.python-eve.org/en/stable/rest_api_for_humans.html )
    -**https://www.merixstudio.com/blog/best-practices-rest-api-development/** (Very clear!!)
    - https://www.merixstudio.com/blog/api-documentation-few-tips-will-help-you-write-it-well/
    - https://dzone.com/articles/api-led-connectivity-with-mule
    - https://blogs.mulesoft.com/learn-apis/api-led-connectivity/what-is-api-led-connectivity/
 
  - Examples:
    - https://github.com/microsoft/api-guidelines
    - https://cloud.google.com/apis/design i http://apistylebook.com/design/guidelines/google-api-design-guide#api-design
    - https://stripe.com/docs/api

  - Tools:
    - [OAS 3.0 editor per Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=42Crunch.vscode-openapi)
    - [Raml](https://raml.org/) Ruled out!!! Do not follow OAS !!
    - [Slate](https://github.com/slatedocs/slate). It seems quite good.
    - [Swagger-UI](https://swagger.io/tools/swagger-ui/)
    - [ReadME](https://readme.com/documentation)
    - [ReDoc](https://github.com/Redocly/redoc): **It allows to publish an API in HTML without having to process**. Only providing the YAML or JSON URL from OAS 3.0.
    - [ApiDocs](https://apidocjs.com/) Very easy but do not say anything about OAS 3.0.
    - [Insomnia](https://github.com/Kong/insomnia) Insomnia is a cross-platform REST client, built on top of Electron. And [look at this link from insomnia](https://support.insomnia.rest/collection/105-inso-cli)
  
  - Comparatives:
    - https://blog.vsoftconsulting.com/blog/is-raml-or-swagger-better-for-building-apis
    - https://nordicapis.com/oas-vs-raml-whats-the-difference/


## About the personalization of APIs for a specific port

Think about how to declare the port for which we want to receive the information. 
- Alternatives: URL from the ws/LOCODE. If there is not a LOCODE, the service will return the information of the local port. For example, http://infoAPI.portic.net/liners/ESBCN or http://infoAPI.portdebarcelona.cat/liners/, accepting also http://infoAPI.portdebarcelona.cat/liners/ESBCN
- First arg from any ws would have to be the LOCODE. 

## About some specific APIs

### Weather

[Guide to marine meteorological services](https://library.wmo.int/index.php?lvl=notice_display&id=7469#.YHGO8uhpEWh)

[Open Weather API](https://openweathermap.org/api) there are examples on how to documment APIs [example](https://openweathermap.org/current)

### Track and trace

[DCSA Track and trace](https://dcsa.org/standards/track-trace/)



[DCSA Track and trace](https://dcsa.org/standards/track-trace/)

### Antwerp API marketplace
- https://www.nxtport.com/market/our-marketplace/marketplace
- https://github.com/NxtPort/API/blob/master/README.md



https://www.youtube.com/watch?v=NzgFdEGI8sI








 
