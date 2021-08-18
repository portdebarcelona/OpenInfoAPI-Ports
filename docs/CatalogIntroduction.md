# Introduction to the catalog of APIs
This catalog enumerates a list of APIs with information about ports that can be useful for the logistic activities and also for the citiens that want to know more about ports.

## Categories

Use of **Categories**. Many concepts are common in all ports (e.g., port services). It is advisable to use a category field that would allow better filtering and precise referencing.

### Ships Calls


![Anchor](https://github.githubassets.com/images/icons/emoji/unicode/2693.png?v8)




Information about vessel's voyages in the port is particularly useful for planning logistic operations, but it can also be useful for acompanying or waiting people that will depart or arrive by ferry or cruise.

This category reffers to all available information about vessels and their voyages within the port, such as their port calls or their voyages, including their stay number and the information about the vessel, such as IMO, lenght, tonnage, .

Possible APIs:
- **Ships Arrival Forecasts**. Forecast of ships that will arrive at a port in a given period of time. 
  - Request parameters: period of time, type of vessel,... 
  - Data included in the response: IMO number, ship name, ETA (Estimated time of arrival), previous port of call,... 
  - [catalog](catalog/catalog-ShipsArrivalForecasts.md)
- **Vessels in port**. Vessels that are anchored/moored in the port. 
  - Request parameters: none. 
  - Data included in the response: IMO number, ship name, ATA (Actual time of arrival), ETD (Estimated Time of Departure), mooring quay, previous port of call,... 
  - [catalog](catalog/catalog-VesselsInPort.md)
- **Ships Exits** Vessels that are sailing up in the next 24 hours or have sailed during the past 24 hours. 
  - Request parameters: none. 
  - Data included in the response: IMO number, ship name, ATD (Actual Time of Departure) or ETD (Estimated Time of Departure), mooring quay, next port of call,... 
  - [catalog](catalog/catalog-ShipExits.md)
- **Ships Arrivals** Vessels that has arrived at a port during the the past 24 hours or will arrive in the next 24 hours. 
  - Request parameters: none. 
  - Data included in the response: IMO number, ship name, ATA (Actual Time of Arrival) or ETA (Estimated time of arrival), previous port of call,... 
  - [catalog](catalog/catalog-ShipsArrivals.md) 
- **Ships Aproximation Manouvres**: Aproximation manouvres of ships to the port. Vessels that have initiated their approximation manouvres. 
  - Request parameters: none. 
  - Data included in the response: IMO number, ship name, ETA (Estimated time of arrival), type of vessel, previous port of call,... 
  - [catalog](catalog/catalog-ShipsAproximationManouvres.md)
- **Ferries Arrivals**: Ferries that has arrived at a port during the the past 24 hours or will arrive in the next 24 hours. 
  - Request parameters: none. 
  - Data included in the response: ship name, ferry operator, ATA (Actual Time of Arrival) or ETA (Estimated time of arrival), previous port of call,...
  - [catalog](catalog/catalog-FerriesArrivals.md)
- **Ferries Departures**: Ferries that have sailed for the past 24 hours or are sailing up in the next 24 hours. 
  - Request parameters: none. 
  - Data included in the response: ship name, ferry operator, ATD (Actual Time of Departure) or ETD (Estimated Time of Departure), mooring quay, next port of call,...
  - [catalog](catalog/catalog-FerriesDepartures.md)
- **Cruises Calls**: Cruise schedules 
  - Request parameters: ship name. 
  - Data included in the response: ship name, cruise line, ETA (Estimated Time of Arrival), ETD (Estimated Time of Departure), cruise terminal,...
  - [catalog](catalog/catalog-CruisesCalls.md)

Benchmarking: [select](Benchmarking.md#ShipCalls)
### Liner Services
The connectivity of a port depends on the list of ports that are serviced periodically. Liner services define the network of ports with direct maritime connections to a port and their periodicity and capacity.

Possible APIs:
- **Liner services**
  - Request parameters: liner service name, shipowner, type of cargo,... 
  - Data included in the response: liner service name, shipowner, type of cargo, periodicity, list of linked ports, capacity (TEU weekly),...
  - [catalog](catalog/catalog-LinerServices.md)

### Port Infrastructure

Geographical/spatial information about the port, land accesses, terminals, and marine aids to navigation.

Possible APIs:
- **Port infrastructure**
  - Request parameters: port name,... 
  - Data included in the response: latitude/longitud, land area, berths (length, depth, loading capacities, contact information),...
  - [catalog](catalog/catalog-PortInfrastructure.md)
- **Port gates**
  - Request parameters: none. 
  - Data included in the response: gate name, latitude/longitud, allowed vehicles, maximun width, maximum height, opening hours,...
  - [catalog](catalog/catalog-PortGates.md)
- **Port terminals**
  - Request parameters: none. 
  - Data included in the response: terminal name, type of terminal (ferry, cruise, container, multipurpose, vehicle, Bulk cargo,...), gate latitude/longitud, allowed vehicles, maximun width, maximum height, opening hours,...
  - [catalog](catalog/catalog-PortTerminals.md)
- **Marine Aids to Navigation**
  - Request parameters: port name, port entrance/port mouth,...
  - Data included in the response: fixed bridges and other structures over navegable waters, identification parameters of those structures, latitude/longitude,...
  - [catalog](catalog/catalog-MarineAids.md)

### Port Procedures (Work in progress)

  ![Ft](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Ft3.png?raw=true)

Certain operations require some procedure instructions and these procedures should be published and accessible to several applications. 

Here are some examples of APIs that can facilitate information of some of these procedures:

- **Customs Controls and Inspections**

  Customs can carry out their physical inspections inside the cargo terminals, at the terminal yard or in a warehouse, but they can also inspect containers, platforms or trucks using a non-intrusive technology as an X-ray scanner. Operators need to know which units have been selected to be inspected by Customs, to know if the inspection has been carried out and whether the goods have been cleared. 
  
  Possible APIs:
  - Customs Inspections
    - Request parameters: equipment id. 
    - Data included in the response: unit of cargo selected for inspection (true/false), type of inspection (intrusive/non-intrusive), place of the inspection (container yard, bonded warehouse,..), status (pending/carried out/cleared,...),...
    - [catalog](catalog/catalog-CustomsInspections.md)   

- **Border Control Posts (BCP)**


  A Border Control Post is an inspection post designated and approved in line with EU legislation for carrying out checks on animals and animal products arriving from third countries at a European Union border. These checks are carried out to protect animal and public health, and animal welfare.
  Operators need to know which units have been selected by the Sanitary Authorities to be inspected, to know if the inspection has been performed and if their goods have been cleared.

  Possible APIs:
  - Border Control Posts
    - Request parameters: equipment id. 
    - Data included in the response: unit of cargo selected for inspection (true/false), border inspection service (phytosanitary, veterinary, pharmacy, health, quality and industrial regulations,...), type of inspection (container emptying, container emptying and classification, identity, inspection, opening but not inspected, "passadís", resealing, resealed but not openned, thermodesinfection, transfer of goods, ventilation, fumigation, fumigation check...), place of the inspection (container yard, border inspection post, designated point of import (DPI), designated point of entry (DPE)), positioning reasons (inspection, customer requirements, others), status (pending/carried out/cleared,...),...
    - [catalog](catalog/catalog-BorderInspections.md)   


- **VGM (Verified Gross Mass)**

  As the International Maritime Organisation (IMO) declare: *"discrepancies between the declared gross mass and the actual gross mass of a packed container could have an adverse impact on the safety of the ship, seafarers and shore-side workers, by leading to incorrect vessel stowage decisions and potentially collapsed container stacks or loss of containers overboard"*.

  The IMO established a requirement that packed containers must be weighed to obtain their actual gross mass prior to vessel loading.  This requirement is included in the Guidelines regarding the verified gross mass of a container carrying cargo (MSC.1/Circ.1475) and the adoption of amendment to SOLAS regulation VI/2 requires the mandatory verification of the gross mass of packed containers (resolution MSC.380(94)).

  The aforementioned SOLAS amendments introduce two main new requirements:
  1. the shipper is responsible for providing the verified weight by stating it in the shipping document and submitting it to the master or his representative and to the terminal representative sufficiently in advance to be used in the preparation of the ship stowage plan; and 
  2. the verified gross mass is a condition for loading a packed container onto a ship.
  
  A prerequisite for the container to be loaded onto a ship to which the SOLAS regulations apply is the availability of the verified gross mass of a packed container sufficiently in advance to the terminal representative and to the master or his representative to be used in the ship stowage plan.  However, it does not constitute an entitlement for loading, because the master retains ultimate discretion in deciding whether to accept a packed container for loading onto his ship.

  The verification of the gross mass can be achieved by either of two methods:
  1. weighing the packed container; or
  2. weighing all packages and cargo items, including the mass of pallets, dunnage and other securing material to be packed in the container and adding the tare mass of the container to the sum of the single masses, using a certified method approved by the competent authority of the State in which packing of the container was completed.

  Possible APIs:

  - VGM
    - Request parameters: equipment id, request of weighting or VGM communication,... 
    - Data included in the response: method of weighting, VGM,...
    - [catalog](catalog/catalog-VGM.md)  

- **Efficiency Network Certificate** 

  ![Efficiency Network](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/EN.png?raw=true)

  Efficiency Network is the brand of the Barcelona Port's quality label.
  The Port of Barcelona every day manages the transportation of thousands of shipments. The job of the Port is to treat each one as it was the only one. To ensure that each shipment receives the treatment it deserves, the Port of Barcelona has created Efficiency Network, a quality brand that identifies the companies operating at the port that adopted a commitment to efficiency to provide the end customers with the utmost satisfaction. It garanties the reliability, transparency and security of all the operations carried out at the Port of Barcelona. Efficiency Network recognises and certifies organisations involved and commited to the most rigorous standards of reliability, so the shipments arrive wherever they need to. A network of people and organisations that join forces with the goal of making the Port of Barcelona a reference, open to the World, commited to a job done well, more effective, more efficient. 
  Efficiency Network has about the destination but also about the path. A more collaborative and competitive path, a path to excellence. 

  Source: Efficiency Network, Port de Barcelona.


  Possible APIs:

  - Certified companies
    - Request parameters: activity, name of the company,... 
    - Data included in the response: name of the company, activities, company certified (true or false),...
    - [catalog](catalog/catalog-EfficiencyNetwork.md)  

- **Container release or acceptance (Container pick-up or delivery from/to the terminal or depot)** 

  ![Camio](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/camio2.png?raw=true)
 
  Container traffic has a big economic impact in ports and the area that they serve.
   
  Container operations in ports are docummented using EDI messages. The EDIFACT container messages are designed to provide standard formats for all functional areas related to the handling and movement of shipping containers and equipment.
  They are divided into two main categories: ship and land operations.
  In this category are included some APIs related with the information exchanged using the EDI messages for land operations with full and empty containers.

  Possible APIs:

  - Container release information (container pick-up from the terminal or depot)
    - Request parameters: container number, full/empty indicator 
    - Data included in the response: container number, full/empty indicator, name of the container terminal or depot, status (pending, authorised, exited,...)...
    - [catalog](catalog/catalog-ContainerRelease.md) 

  - Container acceptance information (container delivery from the terminal or depot)
    - Request parameters: container number, full/empty indicator  
    - Data included in the response: container number, full/empty indicator, name of the container terminal or depot, status (pending, authorised, entered,...)...
    - [catalog](catalog/catalog-ContainerAcceptance.md) 

    




- **Approach instructions** (PENDING)
 
  ![Approach](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/approach3.png?raw=true)

  Port of Barcelona has two entrances - North and South - and each one has its own approach channel.

  APPROACH CHANNELS

    Approach channels consist of two traffic separation schemes guiding ships to/from north and south entrances respectively.
    The separation line of the northern approach channel is indicated by a fairway buoy charted name “November - N” and is equipped with a radio beacon signal (racon) that it appears on X-Band radars as letter “N” of the Morse code.
    The separation line of the southern approach channel is indicated by a fairway buoy charted name “Sierra – S” and is equipped with a radio beacon signal (racon) that it appears on X-Band radars as the letter “B” of the Morse code.

  PRECAUTIONARY AREAS

  Two Precautionary Areas have been set between the end of both approach channels and the port entrances.

  PORT TRAFFIC

  In Barcelona port waters the vessel traffic service (VTS) is provided by ‘Barcelona Port Control’.

  Inbound Vessels-Reporting Points:  
  
  One hour prior to arrival at the fairway buoy ships must contact 'Barcelona Traffic' on VHF channel 10 and "Barcelona Port Control” on VHF channel 14.
  
  Two miles before passing the “Sierra” fairway buoy ships must contact “Barcelona Traffic” on VHF channel 10 and “Barcelona Port Control” on VHF channel 14.
  
  Four miles before passing the “November” fairway buoy ships must contact “Barcelona Traffic” on VHF channel 10 and “Barcelona Port Control” on VHF channel 14.
  
  Nevertheless, the High Speed Crafts must report in both cases when they are four miles off the fairway buoy.

  Outbound or Shifting Vessels-Reporting Points

  One hour before expected departure or shifting, vessels have to contact “Barcelona Port Control” on VHF channel 14.

  Twenty minutes before departure or shifting, vessels have to contact “Barcelona Port Control” on VHF channel 14 in order to request port services and/or obtain permission to depart.

  Passing fairway buoy must contact “Barcelona Traffic” on VHF channel 10 and “Barcelona Port Control”on VHF channel 14.

  Radio Watch
  
  From one hour prior to arrival to two miles away from the “Sierra” fairway buoy or four miles away from “November” fairway buoy and vice versa, ships will maintain a continuous listening watch on VHF channels 10 and 16, and, if possible, VHF channel 14.

  From two miles away from the fairway buoy or four miles away from “November” fairway buoy up to be berthed and vice versa, ships will maintain a continuous listening watch on VHF channels
  14 and 16, and, if possible, VHF channel 10.
  
  OTHER INFORMATION 
  
  Emergency

  In case of emergency on board, the following stations are on permanent duty 24 hours a day:
  - “Barcelona Traffic” on VHF channel 10
  - “Barcelona Port Control” on VHF channel 14

  All ships in the port have to follow the instructions given by Port Emergency Plan authorities unless they have overriding contradictory safety reasons which then have to be immediately reported to the authorities.

  Ships are requested to inform the aforementioned reporting stations any pollution observed on port waters.

  Source: Port Authority of Barcelona

      
  Possible APIs: (PENDING)

    - Approach instructions
      - Request parameters: xxx (tbd)
      - Data included in the response: xxx, ... (tbd)
      - [catalog](catalog/catalog-ApproachInstructions.md) 


### Statistics (PENDING)
![Approach](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/statistics3.png?raw=true)

  Ports are ranked nationally and internationally, and they are compared in many different ways, i.e. by volume or value of trade, the number of TEUs, tones or cruise passengers, revenues, quays length, or storage capacity.

  Moreover, the size of a port, in terms of traffic flow, says nothing about productivity, efficiency, or responsiveness to customers. These are just some of the criteria that a shipper might consider in evaluating port performance. 



  Inspiring webs:
  - Eurostat
    - https://ec.europa.eu/eurostat/databrowser/view/MAR_TF_QM__custom_917144/default/table?lang=en
    - https://ec.europa.eu/eurostat/web/transport/data/database
  - ONU:
    - https://statswiki.unece.org/  (maritime transport is not covered)
    - 
  All the ports have statistical information about the activity. Usually are published annually, monthly, quarterly. Relevant data of a port are:
  - Number ship calls
  - Tones loaded/unloaded
  - Number of containers
  - Vehicles loaded/unloaded
  - Passengers embarked/disembarked
  - Liquid bulks loaded/unloaded
  - Solid bulks loaded/unloaded
  - Economic concepts
  - etc.

### Weather (Work in progress)
![Sun with cloud and rain](https://github.githubassets.com/images/icons/emoji/unicode/1f326.png?v8)  
Several activities at ports, such as berthing, dredging or construction typically require low weather energy conditions for safe execution. 

  Information can assist harbour masters, port pilots, tug masters, mooring officers, and port engineers to make decisions and help them increase safety and efficiency of marine operations in ports.

  Real time information about weather can optimise the scheduling of shipping movements, can minimise weather downtime, can optimise berth use reducing cargo transit delays, can aware of hazardous conditions off coast, can forecast long wave and surging conditions



    ...wind forecasts: trained upon in-port or near-port wind observations, these forecasts let you precisely judge the percentage risk of high winds from one hour ahead to one week ahead.

    Introduction to meteorological data. See [Free Weather APIS to access global weather data](https://rapidapi.com/blog/access-global-weather-data-with-these-weather-apis/), [wheatherapi.com](https://www.weatherapi.com/docs/#apis-realtime)





  Possible APIs: (Work in progress)

  - Realtime weather
    - Request parameters: parameter (temperature, air pressure, wind speed, wind direction, humidity, raifall, illuminance, all), weather station id,... 
    - Data included in the response: Parameter, value, weather station id, latitude and longitude of the sensor, date and time of the data offered.
    - [catalog](catalog/catalog-RealtimeWeather.md) 

- Weather Forecast
    - Request parameters: xxx (tbd) 
    - Data included in the response: xxx (tbd)
    - [catalog](catalog/catalog-WeatherForecast.md) 

- Weather Alerts
    - Request parameters: xxx (tbd) 
    - Data included in the response: xxx (tbd)
    - [catalog](catalog/catalog-WeatherAlerts.md) 


### Sea State (Work in progress)
![Ocean](https://github.githubassets.com/images/icons/emoji/unicode/1f30a.png?v8)

Puertos del Estado offers a service called SAPO (that in Spanish corresponds to the initials of Autonomous Wave Prediction System) to the Port Authorities that request it.

This service allows obtaining a local wave prediction with a horizon of 48 hours considering the transformations induced by the coastline and the continental shelf. The forecast covers a region of about 600 km2 in the area outside the port with a wave generation and scheduling model and the interior area of the port with an agitation model. 




  Possible APIs: (Work in progress)

  - Wave Prediction
    - Request parameters: coordinates, date and time, parameter requested (all, wind speed, wind direction, mar total: Hs(m), Dir, Tp(s), Tz(s), Mar de viento (Hs(m), Dir), Mar de fondo (Hs(m), Dir, Tz(s))),... (to be translated)
    - Data included in the response: coordinates, date and time, value of the parameter requested (),...
    - [catalog](catalog/catalog-WavePrediction.md) 

### Pollution (PENDING)
Publicación en tiempo real [wheather api](https://www.weatherapi.com/docs/#intro-aqi)

- Estimaciones de CO2 emitido en función de las operativas
- Previsión episodios
- Descargas graneles
- **Water quality** 

### Vehicle Traffic (PENDING)
Entradas y salidas de vehículos del recinto portuario

### Train services (o liners) (PENDING)


![Rail tracks](https://github.githubassets.com/images/icons/emoji/unicode/1f6e4.png?v8)

### Train information (PENDING)

- **Train Exits**
- **Train Arrivals**

### Terminals (PENDING)
- Access/Wait time
- Goods/Containers entrance/exit of Terminals
- Vessel Loading/Unloading

### News (PENDING)
![Newspaper](https://github.githubassets.com/images/icons/emoji/unicode/1f4f0.png?v8)

[see 'NewsArticle' at schema.org](https://schema.org/NewsArticle)

### Notices (PENDING)
Often, Port Authorities have to publish some notices (meteorological alerts, port procedures, etc ). Normally these notices are sent by mail and sms, and published in the web. But also is necessary to publish in web services.

Some notices are intended for the port community, and others are intended for the general public. Also, each notice is of interest to some subgroups of the port community, such as ship agents, shipping companies, transport companies, stevedore,  concessionaire, etc.

### Port rates and fees Info (PENDING)


![Spiral notepad](https://github.githubassets.com/images/icons/emoji/unicode/1f5d2.png?v8)
![Money](https://github.githubassets.com/images/icons/emoji/unicode/1f4b0.png?v8)

Summary of rates applicable by the Port Authority:
- Navigation Support Rate (T0)
- Vessel Rate (T1)
- Passenger Rate (T2)
- Cargo Rate (T3)
  - 1. Simplified Modality
  - 2. Modality for Groups of Goods
- Fresh fish Rate (T4)
- Pleasure and Sports Craft Rate (T5)
- Special Use of the Transit Zone Rate (T6)
- Vessel-Generated Waste Collection Service Fee

### Port Services Info (PENDING)

Information about services that are offered by a port. Eg: bunkering, marpol, mooring, pilots, tugs,... (TO DO buscar a la web de l'APB)

Pilotage

  Compulsory for vessels over 500 GT. The service is permanent.
  
Tugs and linesmen

  7 private harbour tugs are available (From 45 to 80 tons of bollard pull). If required tug or linesmen assistance they will be requested through Barcelona Port Control. Tug's line used.
  
Reception Facilities

  There are reception facilities for most residues generated from ships.
  
Buoyage

  IALA Maritime Buoyage System A.

Time
  
  GMT plus 1 hour; GMT plus 2 hours (spring and summer).
  
Social Services for Seamen
  
  “Stella Maris": 34 934431965 (24 hours) Fax 34 934431843  e-mail: apomar@icab.es

  Special Operations

  Special operations like launching lifeboats, cleaning, rinsing or painting of the hull, diving operations, main engine immobilisation, hot works and others must be permitted by port
  authorities. It is recommended applying for permission trough agents in advance -at least 48 hours before arriving or 72 hours before arriving if the special operation is expected during
  weekend or bank holyday -.


### Port Calendar (PENDING)
![Calendar](https://github.githubassets.com/images/icons/emoji/unicode/1f4c6.png?v8)

Information about workdays, local holidays, ... 



### Port Directory (PENDING)
![Office](https://github.githubassets.com/images/icons/emoji/unicode/1f3e2.png?v8)



Logistic services of a port are offered through specialized companies. Also in the port area, some governmental bodies perform several controls.

A port should maintain general information of those companies and governmental bodies, at least covering their contact information and basic information about the services they offer. 

We can implement two APIs in this category: one for creating and updating contact data, and another to publish contact information. This is the classification of port services that have to be used to tag contact info:

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

**Some notes:... Info Open APIs should**:
- Publish kind of services that offer (catalog of services)
- Allow filter companies depending on services that offer
- Alow get information contact of a company (Name, email, phone, address, icon, etc)

[see 'Organization' in schema.org](https://schema.org/Organization)
[evaluate 'Offer' in scehma.org](https://schema.org/Offer)


![Office worker](https://github.githubassets.com/images/icons/emoji/unicode/1f9d1-1f4bc.png?v8)

![Woman office worker](https://github.githubassets.com/images/icons/emoji/unicode/1f469-1f4bc.png?v8)

![Passport](https://github.githubassets.com/images/icons/emoji/unicode/1f6c2.png?v8)

![Ferry](https://github.githubassets.com/images/icons/emoji/unicode/26f4.png?v8)

![Passenger ship](https://github.githubassets.com/images/icons/emoji/unicode/1f6f3.png?v8)