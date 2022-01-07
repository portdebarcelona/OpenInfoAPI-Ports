# NameOfApi specification

## Definition

## Endpoint
## Parameters

## Output 

### Vehicle Traffic Monitoring

Number of vehicles entering or leaving through a certain port gate in a certain period of time. And segregation of this data by type of vehicles. 

Possible APIs:

- **Vehicle traffic monitoring**: Vehicles entering or leaving through a certain port gate in one hour.
  - Request parameters: port name, port UN/LOCODE, type of vehicles (optional), port gate (optional), direction of vehicle flow (optional).
  - Data included in the response: number of vehicles, type of vehicles (optional), port gate (optional), direction of vehicle flow (optional)
  - [catalog](catalog/catalog-Vehicle.md)


### Terminals

This domain will include some operational data related to the performance of the terminals, like their actual access time or some other figures like their dayly or hourly gate movements, at the land side, or information about their movements per hour at the sea side of the terminal. 

Possible APIs:

- **Access/Wait time**: Estimated period of time that trucks have to queue before they can enter into a terminal.
  - Request parameters: port name, port UN/LOCODE, terminal.
  - Data included in the response: number of minutes.
  - [catalog](catalog/catalog-AccessTime.md)
- **Goods/Containers entrance/exit of Terminals**: Number of units (containers, freight cars,...) that enter or leave a terminal per hour during the present day.
  - Request parameters: port name, port UN/LOCODE, terminal, direction of the flow of the units.
  - Data included in the response: number of units, direction of the flow, hour.
  - [catalog](catalog/catalog-AccessTime.md)
- **Vessel Loading/Unloading**: Number of containers loaded or unloaded from a vessel per hour during the present day.
  - Request parameters: port name, port UN/LOCODE, terminal, direction of the flow of the equipments (loading or unloading).
  - Data included in the response: number of units, direction of the flow, hour.
  - [catalog](catalog/catalog-LadingUnloading.md)

### News 

Request of the latest news published by a certain port. It will be also possible to subscribe to a service for recieving the news after indicating an email. 

Possible APIs:

- **Latest news**: Request of the latest news related to certain port.
  - Request parameters: port name, port UN/LOCODE.
  - Data included in the response: Text of the news.
  - [catalog](catalog/catalog-News.md)
- **Latest news subscription**: Subscription to receive the latest news related to certain port.
  - Request parameters: port name, port UN/LOCODE, email.
  - Data included in the response: Subscription confirmation .
  - [catalog](catalog/catalog-NewsSubscription.md)
  


### Notices

Often, Port Authorities have to publish some notices (meteorological alerts, port procedures, etc). Normally these notices are sent by mail and sms, and published in the web. But also is necessary to publish in web services.

Some notices are intended for the port community, and others are intended for the general public. Also, each notice is of interest to some subgroups of the port community, such as ship agents, shipping companies, transport companies, stevedore,  concessionaire, etc.

Possible APIs:

- **Current notices**: List of alerts and notices that are active for a certain port.
  - Request parameters: port name, port UN/LOCODE.
  - Data included in the response: list of notices, including their subject and their content.
  - [catalog](catalog/catalog-Notices.md)
- **Port notices subscription**: Subscription to receive the notices published by a certain port.
  - Request parameters: port name, port UN/LOCODE, email.
  - Data included in the response: Subscription confirmation .
  - [catalog](catalog/catalog-NoticesSubscription.md)


### Port rates and fees Info 

The costs associated to the ship calls and  the flow of goods through ports must be published as part of a transparency policy of those ports.

Bellow there is a summary of the rates applicable by a Spanish Port Authority:
- Navigation Support Rate (T0)
- Vessel Rate (T1)
- Passenger Rate (T2)
- Cargo Rate (T3)
- Fresh fish Rate (T4)
- Pleasure and Sports Craft Rate (T5)
- Special Use of the Transit Zone Rate (T6)
- Vessel-Generated Waste Collection Service Fee

Possible APIs:

- **Ship calls fees**: List of the port rates and fees associated to a ship call at a specific port.
  - Request parameters: port name, port UN/LOCODE.
  - Data included in the response: link to the port website where this information is published.
  - [catalog](catalog/catalog-ShipFees.md)
- **Merchandise fees**: List of the port rates and fees associated to the flow of goods at a specific port.
  - Request parameters: port name, port UN/LOCODE, email.
  - Data included in the response: link to the port website where this information is published.
  - [catalog](catalog/catalog-GoodsFees.md)

### Port Services Info

Information about services that are offered by a port and which vessels can order those services. Eg: bunkering, marpol, mooring, pilots, tugs,...

Possible APIs:

- **Port services**: Characteristics of the port services offered by a port.
  - Request parameters: port name, port UN/LOCODE.
  - Data included in the response: name of the port service, mname of the company that offers that service, phone number, website, vessels that can order the service, main characteristics of that service.
  - [catalog](catalog/catalog-Services.md)


### Port Calendar

The companies and administrations that operate in a port are not always operational. The hours of service and attention to the public of these companies may vary and may even be subject to specific festivities. And this knowledge can be of great help when a particular operation must be carried out through our Port.

Information about working days, weekend days, and list of public holidays from the requested date period and port.

Possible APIs:

- **Port calendar**: Query about the companies that will work on a specific period of time.
  - Request parameters: port name, port UN/LOCODE, name of the company, activity, selected period of time.
  - Data included in the response: json with the name of the company, day of the selected period, opening hours on that day.
  - [catalog](catalog/catalog-Calendar.md)




### Port Directory
Logistic services of a port are offered through specialized companies. Also in the port area, some governmental bodies perform several controls.

A port should maintain general information of those companies and governmental bodies, at least covering their contact information and basic information about the services they offer. 

We can implement two APIs in this domain: one for creating and updating contact data, and another to publish contact information. This is an example of the classification of port services that have to be used to tag contact info:

- **Administration**:
  - Port Authority
  - Harbour Master
  - Customs
  - Border Control Post (BCP)
  - Immigration
- **Warehousing & Logistics**:
  - Container (Depot)
  - Container (CFS)
  - General Cargo
  - Bulk Cargo
  - Temperature controlled
  - Dangerous Cargo
- **Handling**:
  - Container
  - Bulk Cargo
  - Liquid Cargo
  - Multi Purpose
  - Passenger
  - Container (Inland)
- **Carrier**
  - Liner Agent
  - Railway
  - Truck
  - Barge
  - Forwarding Agent
- **Cargo Services**
  - Packaging
  - Stevedoring & Lashing
  - Tally
  - Container
  - Custom Clearance
  - Foodstuff
- **Marine Services**
  - Ship Suppliers
  - Pest control
  - Nautic-technic
  - Tug
  - Mooring
  - Shipyards & Repair
  - Shipowners
  - Pilots
- **Knowledge & Consulting**
  - Education
  - Further Education
  - Research
  - Consulting
  - IT-Service
- **Finance & Trading**
  - Logistics Real Estate
  - Finance & Insurance
  - Container Leasing
  - Trading & Renting
- **Other Suppliers**
  - Marketing & PR
  - Railway Services
  - Manufacturer
  - Health & Social Care

Possible APIs:

- **Create and update the Directory**: Incorporating companies or governmental bodies in the Directory or updating its information.
  - Request parameters: port name, port UN/LOCODE, name of the company, activity, address, phone number, contact e-mail, website.
  - Data included in the response: confirmation of the update and transcription of all the data of that record.
  - [catalog](catalog/catalog-DirectoryUpdate.md)

- **Query the Directory**: Query about a specific company or governmental body.
  - Request parameters: port name, port UN/LOCODE, name of the company/governmental body, file format of the response (json or XML)
  - Data included in the response: json/XML file of all the data of the record of the company selected.
  - [catalog](catalog/catalog-DirectoryQuery.md)


