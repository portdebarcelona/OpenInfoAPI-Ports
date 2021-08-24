# Introduction to the catalog of APIs
This catalog enumerates a list of APIs with information about ports that can be useful for the logistic activities and also for the citiens that want to know more about what is happening in a port.

## Categories

Use of **Categories**. Many concepts are common in all ports (e.g., port services). It is advisable to use a category field that would allow better filtering and precise referencing.

### Ships Calls

![Ship calls](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/ShipCalls.png?raw=true)

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
- **Ships Departures** Vessels that have sailed up or are sailing up today. 
  - Request parameters: none. 
  - Data included in the response: IMO number, ship name, ATD (Actual Time of Departure) or ETD (Estimated Time of Departure), mooring quay, next port of call,... 
  - [catalog](catalog/catalog-ShipDepartures.md)
- **Ships Arrivals** Vessels that has arrived or will arrive at a port today. 
  - Request parameters: none. 
  - Data included in the response: IMO number, ship name, ATA (Actual Time of Arrival) or ETA (Estimated time of arrival), previous port of call,... 
  - [catalog](catalog/catalog-ShipsArrivals.md) 
- **Ships Aproximation Manouvres**: Aproximation manouvres of ships to the port. Vessels that have initiated their approximation manouvres. 
  - Request parameters: none. 
  - Data included in the response: IMO number, ship name, ETA (Estimated time of arrival), type of vessel, previous port of call,... 
  - [catalog](catalog/catalog-ShipsAproximationManouvres.md)
- **Ferries Arrivals**: Ferries that has arrived or will arrive at a port today. 
  - Request parameters: none. 
  - Data included in the response: ship name, ferry operator, ATA (Actual Time of Arrival) or ETA (Estimated time of arrival), previous port of call,...
  - [catalog](catalog/catalog-FerriesArrivals.md)
- **Ferries Departures**: Ferries that have sailed up or are sailing up today. 
  - Request parameters: none. 
  - Data included in the response: ship name, ferry operator, ATD (Actual Time of Departure) or ETD (Estimated Time of Departure), mooring quay, next port of call,...
  - [catalog](catalog/catalog-FerriesDepartures.md)
- **Cruises Calls**: Cruise schedules. 
  - Request parameters: ship name. 
  - Data included in the response: ship name, cruise line, ETA (Estimated Time of Arrival), ETD (Estimated Time of Departure), cruise terminal,...
  - [catalog](catalog/catalog-CruisesCalls.md)


### Liner Services
The connectivity of a port depends on the list of ports that are serviced periodically. Liner services define the network of ports with direct maritime connections to a port and their periodicity and capacity.

Possible APIs:
- **Liner services**: Detailed information about some or all the liner services.
  - Some of the possible request parameters: liner service name, shipowner, port of destination, type of cargo,... 
  - Data included in the response: liner service name, shipowner, type of cargo, periodicity, list of linked ports, capacity (TEU weekly),...
  - [catalog](catalog/catalog-LinerServices.md)

- **Linked ports**: Ports with which the port of reference has liner services (direct connections).
  - Some of the possible request parameters: none.
  - Data included in the response: port name, port code, list of liners,...  
  - [catalog](catalog/catalog-LinkedPorts.md)

- **Carriers/Alliance partners**: Carriers and alliance partners that serve a particular liner service or a geographical area.
  - Some of the possible request parameters: carrier name, carrier code (SCAC), geographical area,...
  - Data included in the response: type of service, frequenct, capacity, duration of service,... 
  - [catalog](catalog/catalog-Carriers.md)

### Port Infrastructure

  ![Porta Europa](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/PortaEU.png?raw=true)

Geographical/spatial information about the port, land accesses, maritime and rail terminals, and marine aids to navigation.

Possible APIs:
- **Port infrastructure**: Basic data of the infrastructure of a port.
  - Request parameters: port name,... 
  - Data included in the response: latitude/longitud, land area, berths (length, depth, loading capacities, contact information),...
  - [catalog](catalog/catalog-PortInfrastructure.md)
- **Port gates**: Information about the main land port accesses. 
  - Request parameters: none. 
  - Data included in the response: gate name, latitude/longitud, allowed vehicles, maximun width, maximum height, opening hours,...
  - [catalog](catalog/catalog-PortGates.md)
- **Maritime terminals**: Information about the maritime terminals of a port.
  - Request parameters: none. 
  - Data included in the response: terminal name, type of terminal (ferry, cruise, container, multipurpose, vehicle, Bulk cargo,...), address, gate latitude/longitud, allowed vehicles, maximun width, maximum height, opening hours,...
  - [catalog](catalog/catalog-PortTerminals.md)
- **Rail terminals and loading tracks**: Information of all the rail terminals and loading tracks of a port.
  - Request parameters: none
  - Data included in the response: list of rail terminals, latitude/longitude, address, type of cargo...
  - [catalog](catalog/catalog-RailwayTerminals.md)
- **Marine aids to navigation** Port marks in a specific port. 
  - Request parameters: none. 
  - Data included in the response: mark, mark number, coordenates situation, apparience during the day, day mark, light phases, comments,...
Observations,...
  - [catalog](catalog/catalog-PortTerminals.md)
- **Bathymetric data** Data from the regular hydrographic surveis that are being performed at ports. 
  - Request parameters: situation (name of the situation -mouth, quay-, coordenates of the situation) 
  - Data included in the response: coordinates, water depth...
Observations,...
  - [catalog](catalog/catalog-Bathymetry.md)

### Port Procedures (Work in progress)

  ![Port processes](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Processos1.png?raw=true)

Certain operations require some procedure instructions and these procedures should be published and accessible to several applications.

The main objective of this category is to make transparent those procedures and to show how to proceed when someone need them.

Here are examples of some procedures and possible APIs that can help operators with those procedures:

- **Customs Clearance for imports**

 ![Customs](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Customs.png?raw=true)

  All shipments of goods entering the European Union from third countries are subject to Customs controls. All goods may be subject to the presentation of several documents and payments, as the payment of Customs duties based on the content of the shipment, payment of national taxes (VAT) or local taxes where applicable, payment of special taxes on tobacco, alcohol, etc., the cost of processing of Single Administrative Document (SAD) for imports, the costs arising from border safety controls, depending on the nature of the shipment (sanitary, pharmaceutical, veterinary, etc.).
  
  As a part of the customs clearance process, customs can carry out docummentary or physical inspections, and those can be carried out inside the cargo terminals, at the terminal yard or in a warehouse, but they can also inspect containers, platforms or trucks using a non-intrusive technology as an X-ray scanner. 
  
  It is the recipient's responsibility to know the conditions for importing their shipment (prohibitions, restrictions, limitations, etc.) and to find out what documents may be required on arrival, including the commercial invoice, certificate of origin, licences and special authorisations for border controls, etc.

  Possible APIs:

  - **Customs clearance procedure**: Resources where can be find information about the procedures for clearing the goods in import.
    - Request parameters: none. 
    - Data included in the response: addresses where information can be found,...
    - [catalog](catalog/catalog-CustomsClearance.md) 

  - **Customs clearance actors**: Contact information of the different actors involved in the customs clearance process.
    - Request parameters: none. 
    - Data included in the response: contact information about Customs, contact information of the operators involved,...
    - [catalog](catalog/catalog-CustomsClearanceContacts.md) 

  - **Customs Inspections** (2n phase of this project) Status of a customs inspection.
    - Request parameters: equipment id. 
    - Data included in the response: unit of cargo selected for inspection (true/false), type of inspection (intrusive/non-intrusive), place of the inspection (container yard, bonded warehouse,..), status (pending/carried out/cleared,...),...
    - [catalog](catalog/catalog-CustomsInspections.md)   

- **Border Controls** (work in progress)

  ![BIP](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/BIP.png?raw=true)

  The border inspection post (BIP) is a controlled and authorised station for customs and sanitary controls of goods. Physical and documentary inspections are carried out at these posts as well as analysis of samples.
  
  A Border Control Post is an inspection post designated and approved in line with EU legislation for carrying out checks on animals and animal products arriving from third countries at a European Union border. These checks are carried out to protect animal and public health, and animal welfare.
  
  As a part of the border clearance process, border inspection services can carry out docummentary or physical inspections, and those can be carried out inside the cargo terminals but usually the physical inspections are carried out at the Border Inspection Posts (BIP), where coexist several specific inspection areas as a designated point of import (DPI), a designated point of entry (DPE) or a border control post (BCP).  
 
  It is the recipient's responsibility to know the conditions for importing their shipment (prohibitions, restrictions, limitations, etc.) and to find out what documents may be required on arrival, including the commercial invoice, certificate of origin, licences and special certifications for border controls, etc.

  Possible APIs: (ckeck the English version)
  - **Procedures for border inspection**: Resources where can be find information about the procedures for clearing the goods subject to controls from the border inspection services.
    - Request parameters: none. 
    - Data included in the response: addresses where information can be found,...
    - [catalog](catalog/catalog-BISClearance.md) 

  - **Border inspection services clearance actors**: Contact information of the different actors involved in the border inspection services clearance process.
    - Request parameters: none. 
    - Data included in the response: contact information about the different border inspection services, contact information of the operators involved,...
    - [catalog](catalog/catalog-BISContacts.md) 
    
  - **Border Control Posts** (2n phase of this project) Status of an inspection from the border inspection services.
    - Request parameters: equipment id. 
    - Data included in the response: unit of cargo selected for inspection (true/false), border inspection service (phytosanitary, veterinary, pharmacy, health, quality and industrial regulations,...), type of inspection (container emptying, container emptying and classification, identity, inspection, opening but not inspected, "passadís", resealing, resealed but not openned, thermodesinfection, transfer of goods, ventilation, fumigation, fumigation check...), place of the inspection (container yard, border inspection post, designated point of import (DPI), designated point of entry (DPE)), positioning reasons (inspection, customer requirements, others), status (pending/carried out/cleared,...),...
    - [catalog](catalog/catalog-BorderInspections.md)   

- **VGM (Verified Gross Mass)**

  ![VGM](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/VGM.png?raw=true)

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

  - **Container tare weight**: The BIC (Bureau International des Containers et du Transport Intermodal) has developed the BoxTech Global Container Database that provides a platform to easily exchange container fleet technical details. BoxTech provides an easy-to-access source of container characteristics like the container number, the size-type code, the tare weight, the maximum gross mass, the maximum payload or the maximum stacking weight.
    - Request parameters: equipment id 
    - Data included in the response: equipment id, tare weight
    - [catalog](catalog/catalog-Tare.md) 

  - **VGM**: (2n phase of this project)
    - Request parameters: equipment id, request of weighting or VGM communication,... 
    - Data included in the response: method of weighting, VGM,...
    - [catalog](catalog/catalog-VGM.md)  

- **Quality Level Certifications**  
 ![Quality](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Quality.png?raw=true)

  Several ports have developed own brands for their quality label schemas.
  There are some ports that every day manage the transportation of thousands of shipments. And the job of each port is to treat each one as it was the only one. To ensure that each shipment receives the treatment it deserves, some ports have created a quality brand that identifies the companies operating at that port that had adopted a commitment to efficiency the end customers with the utmost satisfaction. With this quality level the ports recognise and certify organisations involved and commited to the most rigorous standards of reliability.

  To know which companies have this quality level can be very useful for the users of a port. 

  Possible APIs:
  - **Procedures for being certified with the quality level of a port**.
    - Request parameters: name of the port, code of the port.
    - Data included in the response: tbd
    - [catalog](catalog/catalog-ENProcedures.md) 
    
  - **Certified companies**: List of companies that have been certified by the quality seal managers of a port.
    - Request parameters: name of a port, activity, name of the company,... 
    - Data included in the response: name of the company, activities, company certified (true or false),...
    - [catalog](catalog/catalog-EfficiencyNetwork.md) 

  - **Activities/categories**: List of possible activities, i.e. freight-forwarder, shipping agent, custom broker,...
    - Request parameters: none 
    - Data included in the response: activities name, activity description.
    - [catalog](catalog/catalog-EfficiencyNetwork.md)   

- **Container release or acceptance (Container pick-up or delivery from/to the terminal or depot)**

 ![Exits](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Exits.png?raw=true)
 
  Container traffic has a big economic impact in ports and the area that they serve.
   
  Container operations in ports are docummented using EDI messages. The EDIFACT container messages are designed to provide standard formats for all functional areas related to the handling and movement of shipping containers and equipment.
  They are divided into two main categories: ship and land operations.
  In this category are included some APIs related with the information exchanged using the EDI messages for land operations with full and empty containers.

  Possible APIs:

  - **Container release information (container pick-up from the terminal or depot)**
    - Request parameters: container number, full/empty indicator 
    - Data included in the response: container number, full/empty indicator, name of the container terminal or depot, status (pending, authorised, exited,...)...
    - [catalog](catalog/catalog-ContainerRelease.md) 

  - **Container acceptance information (container delivery from the terminal or depot)**
    - Request parameters: container number, full/empty indicator  
    - Data included in the response: container number, full/empty indicator, name of the container terminal or depot, status (pending, authorised, entered,...)...
    - [catalog](catalog/catalog-ContainerAcceptance.md) 

    

- **Approach instructions** (Work in progress)
 
  ![Approach](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/approach3.png?raw=true)

  Up-to-date information on approach instructions is vital so that maritime operations can be carried out safely.
      
  Possible APIs: 

    - **Approach instructions**: Basic information for the vessels approach to a port
      - Request parameters: name of the port, port code (UN/LOCODE).
      - Data included in the response: Entrances, approach channels, precautionary areas, port traffic (inbound vessels-reporting points, outbound or shifting vessels-reporting points and radio watch), emergency, special operations (like launching lifeboats, cleaning, rinsing or painting of the hull, diving operations, main engine immobilisation, hot works and others), pilotage, tugs, linesmen and last changes in this information.
      - [catalog](catalog/catalog-ApproachInstructions.md) 


### Statistics (Work in progress)

![Chart upward](https://github.githubassets.com/images/icons/emoji/unicode/1f4c8.png?v8)


  Ports are ranked nationally and internationally, and they are compared in many different ways, i.e. by volume or value of trade, the number of TEUs, tones or cruise passengers, revenues, quays length, or storage capacity.

  Moreover, the size of a port, in terms of traffic flow, says nothing about productivity, efficiency, or responsiveness to customers. These are just some of the criteria that a shipper might consider in evaluating port performance. 

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

  And it is also important to define how often the data will be obtained and published.

Possible APIs: 
  - **tbd**: aaaa. 
    - Request parameters: aaa,... 
    - Data included in the response: bbb,...
    - [catalog](catalog/catalog-Statistics.md) 
 

Benchmarking:
- Eurostat
    - https://ec.europa.eu/eurostat/databrowser/view/MAR_TF_QM__custom_917144/default/table?lang=en
    - https://ec.europa.eu/eurostat/web/transport/data/database
- United Nations:
    - https://statswiki.unece.org/  (maritime transport is not covered)
    - Review of maritime transport [UNCTAD](https://unctad.org/es/node/29022)




### Weather
![Sun with cloud and rain](https://github.githubassets.com/images/icons/emoji/unicode/1f326.png?v8)  
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
    - Data included in the response: name of the port, port code (UN/LOCODE), minimum temperature, maximum temperature, rainfall probability,...
    - [catalog](catalog/catalog-WeatherForecast.md) 

- **Weather Alerts**: Weather alerts for a port.
    - Request parameters: name of the port, port code (UN/LOCODE)  
    - Data included in the response: name of the port, port code (UN/LOCODE), active weather alert (true/false), type of weather alert (rainfall, low temperatures, high temperatures, lightning, snow, high winds,...)
    - [catalog](catalog/catalog-WeatherAlerts.md) 

Benchmarking:
- Free Weather APIS to access global weather data:
  - https://rapidapi.com/blog/access-global-weather-data-with-these-weather-apis/)
  - [wheatherapi.com](https://www.weatherapi.com/docs/#apis-realtime)


### Sea State
![Ocean](https://github.githubassets.com/images/icons/emoji/unicode/1f30a.png?v8)

Wave prediction can be used for the prevention of loss of life and property at sea, providing timely and accurate marine weather warnings and forecasts.



Possible APIs: 

  - **Wave Prediction**: Prediction of waves, including the component of the wind waves plus the swell.
    - Request parameters: port name, port code (UN/LOCODE).
    - Data included in the response: port, mouth coordinates, date and time, wind speed, wind direction, waves -total-(wave height Hs(m), direction, wave period Tp(s), wave period Tz(s)), wind waves (wave height Hs(m), direction), swell (wave height Hs(m), direction, period Tz(s)),... 
    - [catalog](catalog/catalog-WavePrediction.md) 

  - **Currents**: Information about the currents near the port and even inside the port waters. Available in https://map.emodnet-physics.eu/ (check pending) 
    - Request parameters: port
    - Data included in the response: ,... 
    - [catalog](catalog/catalog-Currents.md) 

  Benchmarking:
- Europe has also developed a portal that aggregates this kind of information [EMODnet](https://emodnet.ec.europa.eu/en/physics) and is offering several APIs, like this one with all the sources of this kind of information:
  - www.emodnet-physics.eu/map/Service/WSEmodnet2.aspx
  - www.emodnet-physics.eu/map/service/WSEmodnet2.asmx

- Puertos del Estado offers a service called SAPO (that in Spanish corresponds to the initials of Autonomous Wave Prediction System) to the Port Authorities that request it. This service offers a local wave prediction with a horizon of 48 hours considering the transformations induced by the coastline and the continental shelf. The forecast covers a region of about 600 km2 in the area outside the port with a wave generation and scheduling model and the interior area of the port with an agitation model. 
  - http://www.puertos.es/es-es/oceanografia/Paginas/portus.aspx

- [NOOA WAVEWATCH-III.v6.07.1 on GitHub](https://github.com/NOAA-EMC/WW3/releases/tag/6.07.1)

### Pollution (Work in progress)
![Factory](https://github.githubassets.com/images/icons/emoji/unicode/1f3ed.png?v8)

Pollution from ports can affect the air and also the waters. 

Major air pollutants generated by port activities include carbon dioxide (CO2), carbon monoxide (CO), volatile organic compounds (VOCs), nitrogen oxides (NOx), sulfur oxides (SOx), and particulate matter (PM).

Ports concentrate industrial areas next to the water. Many activities such as transportation, terminal operations, cargo handling, storage and boat repair all have potential impacts on water quality if an incident were to occur. In parallel, the many vessels that use the ports to release discharges whilst in transit or alongside. 

- Estimates of CO2 emitted based on operations
- Forecast episodes
- Bulk discharges
- Water quality 

Possible APIs:

- **Pollution**: Current pollution data of a port. 
  - Request parameters: parameter requested (all, air, water, carbon dioxide CO2, carbon monoxide CO, volatile organic compounds (VOCs), nitrogen oxides (NOx), sulfur oxides (SOx), particulate matter (PM), include water parameters), date and time...
  - Data included in the response: value of the parameter requested (), date and time,...
  - [catalog](catalog/catalog-Pollution.md)

Benchmarking:
- WeatherAPI.com provides access to weather and geo data via a JSON/XML restful API. Among others, they provide following data through their API:
  - Real-time weather
  - Weather Alerts 
  - Air Quality Data 
  - [wheather api](https://www.weatherapi.com/docs/#intro-aqi)

### Vehicle Traffic Monitoring (PENDING)
Entradas y salidas de vehículos del recinto portuario

### Rail transport (Work in progress)

![Rail tracks](https://github.githubassets.com/images/icons/emoji/unicode/1f6e4.png?v8)

Rail transport is reliable and extremely suitable for heavy cargoes, including cars, chemical tanks and containers. One train takes an average of 45 trucks off the road. Rail transport for goods makes the logistical chain at the port much more sustainable and efficient. 

Containers are ideal for intermodal transport, including by rail. In intermodal transport, containers arriving by sea can be transported further by rail to their final destination in the hinterland.

Sometime ports have high-frequency rail shuttles between the port and several inland terminals and the knowledge of these rail transport connections is key for port operators.

There are ports with a few dozen trains that arrive or depart everyday and logistic operators need traceability of their movements, including their estimated time of arrival (ETA) and estimated time of departure (ETD).


Possible APIs:

- **Rail transport connections**: Rail connections from a port. 
  - Request parameters: port name, port code (UN/CEFACT).
  - Data included in the response: origin/destination, rail lenght, rail undertaking, type of cargo, frequency, capacity,...
  - [catalog](catalog/catalog-RailConnections.md)

- **Linked railway terminals**: Rail destinations served by one port. 
  - Request parameters: port name, port code (UN/CEFACT).
  - Data included in the response: destination, rail undertaking, type of cargo, frequency, capacity,..
  - [catalog](catalog/catalog-InlandTerminals.md)

- **Railway undertaking**: The rail undertaking is the entity responsible for running the trains and must have a valid license that shows that is authorized to run the train. 
  - Request parameters: tbd...
  - Data included in the response: tbd,...
  - [catalog](catalog/catalog-Undertaking.md)

- **Logistic service provider**: A Logistic Service Provider (LSP) is a provider of logistic services who provides the goods for transport (not necessarily the owner of the goods). The LSP can be a freight forwarder, a shipping agent or a company dedicated exclussivelly to the rail transport of goods.
  - Request parameters: tbd...
  - Data included in the response: tbd,...
  - [catalog](catalog/catalog-LSP.md)

- **Train Arrivals**: Train arrivals for today.
  - Request parameters: tbd...
  - Data included in the response: tbd,...
  - [catalog](catalog/catalog-TrainArrivals.md)

- **Train Departures**: Train departures for today.
  - Request parameters: tbd...
  - Data included in the response: tbd,...
  - [catalog](catalog/catalog-TrainDepartures.md)

Benchmarking:

- https://ontology.tno.nl/smart-rail/ 


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

### Port rates and fees Info (PENDING) (pensar si ho posem a procedures)

![Bookmark tabs](https://github.githubassets.com/images/icons/emoji/unicode/1f4d1.png?v8)

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

### Port Services Info (PENDING) (indicar les empreses)

Information about services that are offered by a port. Eg: bunkering, marpol, mooring, pilots, tugs,... (TO DO buscar a la web de l'APB)

Pilotage

  Compulsory for vessels over 500 GT. The service is permanent.
  
Tugs and linesmen

  7 private harbour tugs are available (From 45 to 80 tons of bollard pull). If required tug or linesmen assistance they will be requested through Barcelona Port Control. Tug's line used.
  
Reception Facilities - waste management

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

The companies and administrations that operate in a port are not always operational. The hours of service and attention to the public of these companies may vary and may even be subject to specific festivities. And this knowledge can be of great help when a particular operation must be carried out through our Port.

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




**Some last  notes:... Info Open APIs should**:
- Publish kind of services that offer (catalog of services)
- Allow filter companies depending on services that offer
- Alow get information contact of a company (Name, email, phone, address, icon, etc)

- [Ontology from TNO](https://ontology.tno.nl/) 

- [see 'Organization' in schema.org](https://schema.org/Organization)
- [evaluate 'Offer' in scehma.org](https://schema.org/Offer)


![Office worker](https://github.githubassets.com/images/icons/emoji/unicode/1f9d1-1f4bc.png?v8)


![Passenger ship](https://github.githubassets.com/images/icons/emoji/unicode/1f6f3.png?v8)

![Anchor](https://github.githubassets.com/images/icons/emoji/unicode/2693.png?v8)


