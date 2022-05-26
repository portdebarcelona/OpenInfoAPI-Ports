# Benchmarking
Conditioned by the commitment to offer services to logistics/port operators and the public, it has been considered appropriate to analyse initiatives from other areas such as port and shipping industry, logistics, government bodies or Smart Cities.

## Port and shipping industry 
- Some initiatives based on APIs are:

### [IPCSA – a network of trusted networks (NoTN)](https://notn.ipcsa.international/)
- IPCSA offers two APIs, Portcall and Cargo Status.

### [DCSA](https://dcsa.org/)
- DCSA have published a series of standards for the container shipping industry, including a common set of processes as well as the data and interfaces for them to be implemented by carriers, shippers and interested third parties, so that communicate digitally in a unified way.
- As part of their standards, they publish API definitions on SwaggerHub, the open-source API development platform, and documentation and version control can be found on GitHub.

### [NxtPort - Port of Antwerp](https://www.nxtport.com/)
- At the time of writing this document, NxtPort has a Marketplace where more than fifteen APIs are offered. E.g. , Green Lights, that checks the different release steps of your container in the import process.
- Most of the APIs defined and developed are in accordance with the OpenAPI specification, some of them in version 2 and others in version 3.

### [Digital LAB - Port of Rotterdam](https://lab.portofrotterdam.com/api)
- The API services that are under development are presented on the Digital LAB website of the Port of Rotterdam. E.g. BoxInsider: Receive updates about your container journeys from port to door and vice versa via the Port of Rotterdam

### [myTerminal (ECT Rotterdam)](https://myterminal.ect.nl/)
- From the ECT terminals in Rotterdam, offers access to up-to-date information on terminal activity. E.g. information on the estimated date of unloading of the containers.

### [TradeLens API](https://knowledge.tradelens.com/hc/en-us/categories/4404458990353-TRADELENS-APIs) 

- Tradelens is a collaboration between Maersk and IBM to create a platform to share and optimize shipment information between shipping lines, companies, and different authorities. 
- They have a set of queries about shipments (Consignment Queries) and another about containers (Transport Equipment Queries) that have been documented using Swagger 2.0 (equivalent to Open API 2.0).
- To access its APIs, the Tradelens service must be contracted.

### [Bureau International des Containers (BIC)](https://www.bic-code.org/)

- The Bureau International des Containers provides standards for sea containers. Its standardized codes can be used by any party involved in the supply chain, facilitating communication between the parties involved in a unified and unambiguous way. BIC provides these codes via API so that other applications can create services for the container shipping industry. E.g. Boxtech. Database with the characteristics of the containers, accessible from their license plate. 

## National and international organizations and institutions
### [UNdata](https://data.un.org/Host.aspx?Content=API)
- The UNdata API provides access to data within the UNdata platform. Developers can use the API to dynamically query UNdata for the latest data and display the result on a web page, download it to local storage for further processing, etc.

### [datos.gob.es](https://datos.gob.es/en/apidata)

- Open information is provided with documentation of the API's methods, parameters, and interactive model, and test queries can be made:
https://datos.gob.es/es/accessible-apidata.

### [EDI3 Standards](https://edi3.org/)

- They offer standards for the supply chain and tools for web developers.
Most international electronic business transactions today are implemented using the standards defined by UN/CEFACT, such as EDIFACT and XML schemas.
The purpose of EDI3 Standards is to make semantic standards incorporate all pre-existing knowledge of the business domain and make it accessible to web developers. The site also supports interoperable implementations through open tools.
- All this information can be very useful for web developers.
- Semantic and technical specifications are published on its website, as well as tools and methods.

## Smart cities
### [FIWARE](https://www.fiware.org)

- FIWARE is defined as an open-source platform component framework to accelerate the development of intelligent solutions. As indicated on its own website, the FIWARE Foundation promotes the definition, and the open-source implementation, of key open standards that allow the development of portable and interoperable smart solutions in a faster, easier, and more affordable way, avoiding blocking scenarios of suppliers, while also fostering FIWARE as a sustainable and innovation-driven business ecosystem.
- FIWARE offers a set of open-source components that can be assembled or with third party components to build platforms that support the development of Smart solutions faster, easier, and cheaper. The only essential component is a “FIWARE Context Broker Generic Enabler”.
- They have also promoted the joint initiative "Smart Data Models" between the FIWARE Foundation, the TM Forum, IUDX and OASC to support the adoption of a reference architecture and compatible common data models that support a digital market of interoperable and replicable smart solutions in multiple sectors, starting with Smart Cities. The “Smart Data Models” include three elements: the schema or technical representation of the model that defines the structure and types of technical data, the specification of a document written to be read by people and the content examples for the NGSIv2 and NGSIv2 versions. NGSI-LD.
- The acronym NGSI stands for "Next Generation Service Interfaces", a set of specifications originally issued by the Open Mobile Alliance (OMA) that included context interfaces. These were adopted and developed as NGSIv2 by the European Future Internet Public-Private-Partnership (PPP), which spawned the FIWARE open-source community.
- All data models are public and copyright free.

## Other initiatives related to the Domains of this project
### Free APIs to access global weather data 
- [Top 8 Best Free Weather APIs to Access Global Weather Data (Updated for 2022)](https://rapidapi.com/blog/access-global-weather-data-with-these-weather-apis/)
- [WeatherAPI.com](https://www.weatherapi.com/docs/#apis-realtime)  
- [Meteomatics](https://www.meteomatics.com/en/api/getting-started/)

### References on the sea state
**EMODnet**
- Europe has developed a website that aggregates several portals, one with this type of information is [EMODnet](https://emodnet.ec.europa.eu/en/physics) where several APIs are offered, such as one with all the sources of this type of information:
•	www.emodnet-physics.eu/map/Service/WSEmodnet2.aspx
•	www.emodnet-physics.eu/map/service/WSEmodnet2.asmx

**Puertos del Estado**
- Puertos del Estado offers a service called [SAPO](http://www.puertos.es/es-es/oceanografia/Paginas/portus.aspx) (in Spanish Sistema Autónomo de Predicción del Oleaje - Autonomous Wave Prediction System) to the Port Authorities that request it. This service offers a local wave forecast with a horizon of 48 hours considering the transformations induced by the coastline and the continental shelf. The forecast covers a region of about 600 km2 in the outer area of the port with a wave generation and programming model and the inner area of the port with an agitation model 

### Some references on pollution data
- WeatherAPI.com provides access to weather and geographic data through the JSON/XML restful API. Among others, it provides the following data through its API:
  - Real-time weather
  - Weather Alerts
  - [Air Quality Data](https://www.weatherapi.com/docs/#intro-aqi) 