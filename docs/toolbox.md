# Toolbox
The toolbox is a uniform set of tools for the API specification, independent from the application domain (trade, port infrastructure, procedures, weather, companies’ directory, news, etc.).


Given that one of the objectives of the project is that it will be easily replicable and understanding that the cost of the tools could be a handicap for its achievement, it has been adopted, as a premise, that all the tools necessary for the development of the project will be `open source`.

Here, we explain which tools we use. Each decision has been the result of a balance between its functionalities and its ease of use.

## [GitHub](https://github.com/) 
- The documentation of the project and the APIs have been published on Github, the portal that allows the registration and control of all the changes made, and allows other users to download their definitions, have access to their documentation and contribute to its development.
- For this project, a specific repository was created in the Port of Barcelona account, where all its documentation is: https://github.com/portdebarcelona/OpenInfoAPI-Ports
## [Visual Studio Code](https://code.visualstudio.com/) 
- Visual Studio Code is a source code editor developed by Microsoft that offers several features that facilitate code development and includes the possibility of adding extensions such as the ones used for editing the markdown documents or defining an API compliant with the OpenAPI specification.
## [SwaggerUI](https://swagger.io/tools/swagger-ui/)
- Swagger's UI allows you to view and interact with this project's API resources without having any implementation logic developed. 
- It is automatically generated from the OpenAPI specification and makes it easy to implement on the back end and consume on the client side.
In this project, the API that incorporates all the methods of the identified domains has been published in: https://app.swaggerhub.com/apis/openinfoapiports/oiap/
## [RapiPDF](https://mrin9.github.io/RapiPdf/)
- Online tool that can document APIs in pdf from their OpenAPI specifications.
## [cloudconvert](https://cloudconvert.com/md-to-docx)
- This online document format conversion tool has been used to convert GitHub's MD extension files to Word files.
