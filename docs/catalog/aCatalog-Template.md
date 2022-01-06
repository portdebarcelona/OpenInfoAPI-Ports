# NameOfApi specification

## Definition

## Endpoint
## Parameters

## Output 



- **Approach instructions** 
 
  Up-to-date information on approach instructions is vital so that maritime operations can be carried out safely.
      
  Possible APIs: 

    - **Approach instructions**: Basic information for the approach of the vessels to a port
      - Request parameters: name of the port, port code (UN/LOCODE).
      - Data included in the response: Entrances, approach channels, precautionary areas, port traffic (inbound vessels-reporting points, outbound or shifting vessels-reporting points and radio watch), emergency, special operations (like launching lifeboats, cleaning, rinsing or painting of the hull, diving operations, main engine immobilisation, hot works and others), pilotage, tugs, linesmen and last changes in this information.
      - [catalog](catalog/catalog-ApproachInstructions.md) 


### Statistics 

  Ports are ranked nationally and internationally, and they are compared in many different ways, i.e. by volume or value of trade, the number of TEUs, tones or cruise passengers, revenues, quays length, or storage capacity.

  All the ports have statistical information about the activity. Relevant data of a port can be:
  - Value of goods passing through the port (euros)
  - Number of ship calls (stopovers)
  - Tones loaded/unloaded by sector (energy, vehicles and transport elements, agro-livestock and food, chemicals, iron and steel, building materials, fertilisers, non-metallic minerals, other goods)
  - Traffic by geographical areas (total, main destination areas and main areas of origin)(tones)
  - Goods by type of packaging and shipping (container load, conventional charge, liquid bulk or dry bulk)(tones)
  - Container traffic (all, full/empty, import/export)(TEU)
  - Vehicles loaded/unloaded (units)
  - Liquid bulk loaded/unloaded (tones)
  - Solid bulk loaded/unloaded (tones)
  - Short sea shipping (intermodal transport units (UTI))
  - Container rail traffic (TEU)
  - Container rail share (%)
  - Vehicle rail traffic (units)
  - Vehicle rail share (%) 
  - Passengers embarked/disembarked (units)
  - Cruise passengers embarked/disembarked (units)
  - Economic concepts:
    - Turnover (thousand euro)
    - Port fees (thousand euro)
    - Operating income (thousand euro)
    - Expenditure (thousand euro)
    - Financial result (thousand euro)
    - Financial income (thousand euro)
    - Financial expenses (thousand euro)
    - Earnings Before Interest, Taxes, Depreciation, and Amortisation (EBITDA) (thousand euro)
    - Cash flow (thousand euro)
    - Investment (thousand euro)
    - Long term debt (thousand euro)
  - etc.

  And it is also important to know how often the data can be obtained and published.

Possible APIs: 
  - **Traffic statistics**: Statistics of traffic from a port.
    - Request parameters: port name, port UN/LOCODE, period of time, dimension, level of aggregation.   
    - Data included in the response: data requested as json.
    - [catalog](catalog/catalog-Statistics.md) 

  - **Economic data**: Economic data of a port. 
    - Request parameters: port name, port UN/LOCODE, period of time, dimension, level of aggregation.    
    - Data included in the response: data requested as json.
    - [catalog](catalog/catalog-EconomicData.md) 
 

### Environment: Weather
 
Several activities at ports, such as berthing, dredging or construction typically require low weather energy conditions for safe execution. 

  Information can assist harbour masters, port pilots, tug masters, mooring officers, and port engineers to make decisions and help them increase safety and efficiency of marine operations in ports.

  Real time information about weather can optimise the scheduling of shipping movements, can minimise weather downtime, can optimise berth use reducing cargo transit delays, can aware of hazardous conditions off coast, can forecast long wave and surging conditions


  Possible APIs: 
  - **Realtime weather**: Realtime weather of the default weather station of a port. 
    - Request parameters: name of the port, port code (UN/LOCODE), parameter (all, temperature, air pressure, wind speed, wind direction, humidity, raifall, illuminance, all), weather station id,... 
    - Data included in the response: Parameter, value, port name, port code (UN/LOCODE), weather station id, latitude and longitude of the sensor, date and time of the data offered.
    - [catalog](catalog/catalog-RealtimeWeather.md) 

- **Weather Forecast**: 5 days weather forecast for a port
    - Request parameters: name of the port, port code (UN/LOCODE) 
    - Data included in the response: It returns upto next 5 day weather forecast as json. It contains name of the port, port code (UN/LOCODE), minimum temperature, maximum temperature, rainfall probability,...
    - [catalog](catalog/catalog-WeatherForecast.md) 

- **Weather Alerts**: Weather alerts for a port.
    - Request parameters: name of the port, port code (UN/LOCODE)  
    - Data included in the response: name of the port, port code (UN/LOCODE), active weather alert (true/false), type of weather alert (rainfall, low temperatures, high temperatures, lightning, snow, high winds,...)
    - [catalog](catalog/catalog-WeatherAlerts.md) 

- **Astronomy**: Up to date information for sunrise, sunset, moonrise, moonset, moon phase and illumination.
    - Request parameters: name of the port, port code (UN/LOCODE)  
    - Data included in the response: name of the port, port code (UN/LOCODE), sunrise, sunset, moonrise, moonset, moon phase and illumination.
    - [catalog](catalog/catalog-Astronomy.md) 



### Environment: Sea State

Wave prediction can be used for the prevention of loss of life and property at sea, providing timely and accurate marine weather warnings and forecasts.

Possible APIs: 

  - **Wave Prediction**: Prediction of waves, including the component of the wind waves plus the swell.
    - Request parameters: port name, port UN/LOCODE.
    - Data included in the response: port, mouth coordinates, date and time, wind speed, wind direction, waves -total-(wave height Hs(m), direction, wave period Tp(s), wave period Tz(s)), wind waves (wave height Hs(m), direction), swell (wave height Hs(m), direction, period Tz(s)),... 
    - [catalog](catalog/catalog-WavePrediction.md) 

  - **Currents and tides**: Information about the currents and tides at the entrance mouths.
    - Request parameters: port name, port UN/LOCODE.
    - Data included in the response: maximum tide, hour of the maximum tide, minimum tide, hour of the minimum tide, current at the entrance mouth (m/s), direction of the current at the entrance mouth (degrees). 
    - [catalog](catalog/catalog-Currents.md) 



### Environment: Pollution 

Pollution from port activities can affect the quality of the air and also the waters. Environmental noise is also another kind of pollution from ports. 

Major air pollutants generated by port activities include carbon dioxide (CO2), carbon monoxide (CO), volatile organic compounds (VOCs), nitrogen oxides (NOx), sulfur oxides (SOx), and particulate matter (PM).

Ports also concentrate industrial areas next to the water and many activities of the ports, such as transportation, terminal operations, cargo handling, storage and boat repair all can have potential impacts on water quality if an incident were to occur.  

The presence in ports of diverse sound from ships, trucks, cranes and also from industrial and ship-yards activities as well as auxiliary services produces negative effects on natural ecosystem and the urban population. This is the noise poññution.

Possible APIs:

- **Pollution**: Current air and water quality of a port. 
  - Request parameters: parameter requested (all, air, water, carbon dioxide CO2, carbon monoxide CO, volatile organic compounds (VOCs), nitrogen oxides (NOx), sulfur oxides (SOx), particulate matter (PM), water parameters (Ammonia, Biochemical Oxygen Demand - BOD-, Blue Green Algae, CDOM-fDOM, Chloride, Chlorophyll, Colorimetry & Photometry Parameters, Conductivity, Dissolved Oxygen, Nitrate,Oil-Hydrocarbon, ORP-Redox, pH, Phosphorus, Photosynthetic Active Radiation (PAR), Rhodamine, Turbidity)), and noise parameters (dB).
  - Data included in the response: value of the parameter requested (carbon dioxide CO2, carbon monoxide CO, volatile organic compounds (VOCs), nitrogen oxides (NOx), sulfur oxides (SOx), particulate matter (PM), include water parameters), noise (dB) date and time.
  - [catalog](catalog/catalog-Pollution.md)



### Rail transport

Rail transport is reliable and extremely suitable for heavy cargoes, including cars, chemical tanks and containers. One train takes an average of 45 trucks off the road. Rail transport for goods makes the logistical chain at the port much more sustainable and efficient. 

Containers are ideal for intermodal transport, including by rail. In intermodal transport, containers arriving by sea can be transported further by rail to their final destination in the hinterland.

Sometime ports have high-frequency rail shuttles between the port and several inland terminals and the knowledge of these rail transport connections is key for port operators.

There are ports with a few dozen trains that arrive or depart everyday and logistic operators need traceability of their movements, including their estimated time of arrival (ETA) and estimated time of departure (ETD).


Possible APIs:

- **Rail transport connections**: Rail connections from a port. 
  - Request parameters: port name, port UN/LOCODE.
  - Data included in the response: origin/destination, rail lenght, rail undertaking, type of cargo, frequency, capacity,...
  - [catalog](catalog/catalog-RailConnections.md)

- **Linked railway terminals**: Rail destinations served by one port. 
  - Request parameters: port name, port UN/LOCODE.
  - Data included in the response: destination, rail undertaking, type of cargo, frequency, capacity,..
  - [catalog](catalog/catalog-InlandTerminals.md)

- **Rail undertaking**: The rail undertaking is the entity responsible for running the trains and must have a valid license that shows that is authorized to run the train. 
  - Request parameters: port name, port UN/LOCODE.
  - Data included in the response: rail undertaking, contact information,...
  - [catalog](catalog/catalog-Undertaking.md)

- **Logistic service provider**: A Logistic Service Provider (LSP) is a provider of logistic services who provides the goods for transport (not necessarily the owner of the goods). The LSP can be a freight forwarder, a shipping agent or a company dedicated exclussivelly to the rail transport of goods.
  - Request parameters: port name, port UN/LOCODE.
  - Data included in the response: logistic service provider, contact information,...
  - [catalog](catalog/catalog-LSP.md)

- **Train Arrivals**: Train arrivals for today.
  - Request parameters: port name, port UN/LOCODE.
  - Data included in the response: Estimated time of arrival (ETA), origin, logistic service provider, rail undertaking, type of cargo,...
  - [catalog](catalog/catalog-TrainArrivals.md)

- **Train Departures**: Train departures for today.
  - Request parameters: port name, port UN/LOCODE.
  - Data included in the response: Estimated time of departure (ETD), destination, logistic service provider, rail undertaking, type of cargo,...
  - [catalog](catalog/catalog-TrainDepartures.md)



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


