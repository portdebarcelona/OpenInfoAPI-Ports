# Catalog of APIs
This catalog enumerates a list of APIs with information about ports that can be useful for the logistic activities and also for the citiens that want to know more about what is happening in a port.

## Domains

Use of **Domains**. Many concepts are common in all ports (e.g., port services). It is advisable to use a domain field that would allow better filtering and precise referencing.

### Ships Calls

![Ship calls](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/ShipCalls.png?raw=true)

Information about vessel's voyages in the port is particularly useful for planning logistic operations, but it can also be useful for acompanying or waiting people that will depart or arrive by ferry or cruise.

This domain reffers to all available information about vessels and their voyages within the port, such as their port calls or their voyages, including their stay number and the information about the vessel, such as IMO, lenght, tonnage, .

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
  - [catalog](catalog/catalog-ShipArrivals.md) 
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

  ![Network](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Network.png?raw=true)

The connectivity of a port depends on the list of ports that are serviced periodically. Liner services define the network of ports with direct maritime connections to a port and their periodicity and capacity.

Possible APIs:
- **Liner services**: Detailed information about some or all the liner services.
  - Some of the possible request parameters: name of port, port UN/LOCODE, liner service name, shipowners/carriers, type of cargo (container, ro-ro),... 
  - Data included in the response:liner service name, shipowners/carriers, type of cargo (container, ro-ro), periodicity, list of linked ports, capacity (TEU weekly),...
  - [catalog](catalog/catalog-LinerServices.md)

- **Linked ports**: Ports with which the port of reference has liner services (direct connections).
  - Some of the possible request parameters: none, filter by geographical area,...
  - Data included in the response: port name, port code, list of liners,...  
  - [catalog](catalog/catalog-LinkedPorts.md)

- **Carriers/Alliance partners**: Carriers and alliance partners that serve a particular liner service or a geographical area.
  - Some of the possible request parameters: carrier name, carrier code (SCAC), geographical area,...
  - Data included in the response: type of service, frequenct, capacity, duration of service,... 
  - [catalog](catalog/catalog-Carriers.md)

### Port Infrastructure

  ![Porta Europa](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/PortaEU.png?raw=true)

Geographical/spatial information about the port, land accesses, berths, depth, maritime and rail terminals, and marine aids to navigation.

Possible APIs:
- **Port infrastructure**: Basic data of the infrastructure of a port.
  - Request parameters: port name,port UN/LOCODE.
  - Data included in the response: latitude/longitud, land area, berths (length, depth, loading capacities, contact information), port entrance mouths (width, depth and orientation)...
  - [catalog](catalog/catalog-PortInfrastructure.md)
- **Port gates**: Information about the main land port accesses. 
  - Request parameters: none. 
  - Data included in the response: gate name, latitude/longitud, allowed vehicles, maximun width, maximum height, opening hours,...
  - [catalog](catalog/catalog-PortGates.md)
- **Berths**: Information about the berths of a port. 
  - Request parameters: none. 
  - Data included in the response: berth name, berth code, lenght, depth,...
  - [catalog](catalog/catalog-Berths.md) 
-**Maritime terminals**: Information about the maritime terminals of a port.
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
  - [catalog](catalog/catalog-MarineAids.md)
- **Bathymetric data** Data from the regular hydrographic surveis that are being performed at ports. 
  - Request parameters: situation (name of the situation -mouth, quay-, coordenates of the situation) 
  - Data included in the response: coordinates, water depth...
Observations,...
  - [catalog](catalog/catalog-Bathymetry.md)

### Port Procedures

  ![Process](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/process.png?raw=true)

Certain operations require some procedure instructions and these procedures should be published and accessible to several applications.

The main objective of this domain is to make transparent those procedures and to show how to proceed when someone need them.

Here are examples of some procedures and possible APIs that can help operators with those procedures:

- **Customs Clearance for imports**

  ![Customs](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Customs.png?raw=true)

  All shipments of goods entering the European Union from third countries are subject to Customs controls. All goods may be subject to the presentation of several documents and payments, as the payment of Customs duties based on the content of the shipment, payment of national taxes (VAT) or local taxes where applicable, payment of special taxes on tobacco, alcohol, etc., the cost of processing of Single Administrative Document (SAD) for imports, the costs arising from border safety controls, depending on the nature of the shipment (sanitary, pharmaceutical, veterinary, etc.).
  
  As a part of the customs clearance process, customs can carry out docummentary or physical inspections, and those can be carried out inside the cargo terminals, at the terminal yard or in a warehouse, but they can also inspect containers, platforms or trucks using a non-intrusive technology as an X-ray scanner. 
  
  It is the recipient's responsibility to know the conditions for importing their shipment (prohibitions, restrictions, limitations, etc.) and to find out what documents may be required on arrival, including the commercial invoice, certificate of origin, licences and special authorisations for border controls, etc.

  Possible APIs:

  - **Customs clearance procedure**: Resources where the procedures for clearing the goods in import can be found. 
    - Request parameters: none. 
    - Data included in the response: Resources where information can be found,...
    - [catalog](catalog/catalog-CustomsClearance.md) 

  - **Customs clearance actors**: Contact information of the different actors involved in the customs clearance process.
    - Request parameters: none. 
    - Data included in the response: contact information about Customs, contact information of the operators involved,...
    - [catalog](catalog/catalog-CustomsClearanceContacts.md) 

  - **Customs Inspections** (2n phase of this project) Status of a customs inspection.
    - Request parameters: equipment id. 
    - Data included in the response: unit of cargo selected for inspection (true/false), type of inspection (intrusive/non-intrusive), place of the inspection (container yard, bonded warehouse,..), status (pending/carried out/cleared,...),...
    - [catalog](catalog/catalog-CustomsInspections.md)   

- **Border Controls**

  ![BIP](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/BIP.png?raw=true)

  The border inspection post (BIP) is a controlled and authorised station for customs and sanitary controls of goods. Physical and documentary inspections are carried out at these posts as well as analysis of samples.
  
  A Border Control Post is an inspection post designated and approved in line with EU legislation for carrying out checks on animals and animal products arriving from third countries at a European Union border. These checks are carried out to protect animal and public health, and animal welfare.
  
  As a part of the border clearance process, border inspection services can carry out docummentary or physical inspections, and those can be carried out inside the cargo terminals but usually the physical inspections are carried out at the Border Inspection Posts (BIP), where coexist several specific inspection areas as a designated point of import (DPI), a designated point of entry (DPE) or a border control post (BCP).  
 
  It is the recipient's responsibility to know the conditions for importing their shipment (prohibitions, restrictions, limitations, etc.) and to find out what documents may be required on arrival, including the commercial invoice, certificate of origin, licences and special certifications for border controls, etc.

  Possible APIs:
  - **Procedures for border inspection**: Resources where the procedures for clearing the goods subject to controls from the border inspection services can be found. 
    - Request parameters: none. 
    - Data included in the response: Resources where information can be found,...
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

  - **VGM procedures**: Resources where the VGM procedures can be found.
    - Request parameters: none. 
    - Data included in the response: Resources where the VGM procedures can be found,...
    - [catalog](catalog/catalog-VgmProcedures.md) 

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
    - Request parameters: name of the port, UN/LOCODE of the port.
    - Data included in the response: Resources where the certification procedure can be found.
    - [catalog](catalog/catalog-ENProcedures.md) 
    
  - **Certified companies**: List of companies that have been certified by the quality seal managers of a port.
    - Request parameters: name of a port, activity, name of the company,... 
    - Data included in the response: name of the company, activities, company certified (true or false),...
    - [catalog](catalog/catalog-EfficiencyNetwork.md) 

  - **Activities/categories**: List of possible activities, i.e. freight-forwarder, shipping agent, custom broker,...
    - Request parameters: none 
    - Data included in the response: activity name, activity description.
    - [catalog](catalog/catalog-Activity.md)   

- **Container release or acceptance (Container pick-up or delivery from/to the terminal or depot)**

  ![Exits](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Exits2.png?raw=true)
 
    Container traffic has a big economic impact in ports and the area that they serve.

    Logistic operators need to know the procedures that they have to follow for pick-up containes from a port or to delivery them. 

    In this domain are included some APIs related with the information exchanged using the EDI messages for land operations with full and empty containers.

  Possible APIs:

  - **Procedures for pick-up or delivery containers from/to the terminal or depot**.
    - Request parameters: name of the port, UN/LOCODE of the port.
    - Data included in the response: Resources where the procedures can be found.
    - [catalog](catalog/catalog-ESMTProcedures.md) 

  - **Container release information (container pick-up from the terminal or depot)**
    - Request parameters: container number, full/empty indicator 
    - Data included in the response: container number, full/empty indicator, name of the container terminal or depot, status (pending, authorised, exited,...)...
    - [catalog](catalog/catalog-ContainerRelease.md) 

  - **Container acceptance information (container delivery from the terminal or depot)**
    - Request parameters: container number, full/empty indicator  
    - Data included in the response: container number, full/empty indicator, name of the container terminal or depot, status (pending, authorised, entered,...)...
    - [catalog](catalog/catalog-ContainerAcceptance.md) 

- **Approach instructions** 
 
  ![Approach](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/approach3.png?raw=true)

  Up-to-date information on approach instructions is vital so that maritime operations can be carried out safely.
      
  Possible APIs: 

    - **Approach instructions**: Basic information for the approach of the vessels to a port
      - Request parameters: name of the port, port code (UN/LOCODE).
      - Data included in the response: Entrances, approach channels, precautionary areas, port traffic (inbound vessels-reporting points, outbound or shifting vessels-reporting points and radio watch), emergency, special operations (like launching lifeboats, cleaning, rinsing or painting of the hull, diving operations, main engine immobilisation, hot works and others), pilotage, tugs, linesmen and last changes in this information.
      - [catalog](catalog/catalog-ApproachInstructions.md) 


### Statistics 

![Chart upward](https://github.githubassets.com/images/icons/emoji/unicode/1f4c8.png?v8)


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
![Ocean](https://github.githubassets.com/images/icons/emoji/unicode/1f30a.png?v8)

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

![Pollution](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Pollution.png?raw=true)

Pollution from port activities can affect the quality of the air and also the waters. Environmental noise is also another kind of pollution from ports. 

Major air pollutants generated by port activities include carbon dioxide (CO2), carbon monoxide (CO), volatile organic compounds (VOCs), nitrogen oxides (NOx), sulfur oxides (SOx), and particulate matter (PM).

Ports also concentrate industrial areas next to the water and many activities of the ports, such as transportation, terminal operations, cargo handling, storage and boat repair all can have potential impacts on water quality if an incident were to occur.  

The presence in ports of diverse sound from ships, trucks, cranes and also from industrial and ship-yards activities as well as auxiliary services produces negative effects on natural ecosystem and the urban population. This is the noise pollution.

Possible APIs:


- **Pollution**: Current air and water quality of a port. 
  - Request parameters: parameter requested (all, air, water, carbon dioxide CO2, carbon monoxide CO, volatile organic compounds (VOCs), nitrogen oxides (NOx), sulfur oxides (SOx), particulate matter (PM), water parameters (Ammonia, Biochemical Oxygen Demand - BOD-, Blue Green Algae, CDOM-fDOM, Chloride, Chlorophyll, Colorimetry & Photometry Parameters, Conductivity, Dissolved Oxygen, Nitrate,Oil-Hydrocarbon, ORP-Redox, pH, Phosphorus, Photosynthetic Active Radiation (PAR), Rhodamine, Turbidity)), and noise parameters (dB).
  - Data included in the response: value of the parameter requested (carbon dioxide CO2, carbon monoxide CO, volatile organic compounds (VOCs), nitrogen oxides (NOx), sulfur oxides (SOx), particulate matter (PM), include water parameters), noise (dB) date and time.
  - [catalog](catalog/catalog-Pollution.md)

- **Noise**: Level of noise of a port. 
  - Request parameters: noise parameters (dB).
  - Data included in the response: noise (dB) date and time.
  - [catalog](catalog/catalog-Noise.md)


### Rail transport

![Rail](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Rail.png?raw=true)

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

![Vehicle](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Vehicle.png?raw=true)

Number of vehicles entering or leaving through a certain port gate in a certain period of time. And segregation of this data by type of vehicles. 

Possible APIs:

- **Vehicle traffic monitoring**: Vehicles entering or leaving through a certain port gate in one hour.
  - Request parameters: port name, port UN/LOCODE, type of vehicles (optional), port gate (optional), direction of vehicle flow (optional).
  - Data included in the response: number of vehicles, type of vehicles (optional), port gate (optional), direction of vehicle flow (optional)
  - [catalog](catalog/catalog-Vehicle.md)


### Terminals
![Bulk](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Bulk2.png?raw=true)

This domain will include some operational data related to the performance of the terminals, like their actual access time or some other figures like their dayly or hourly gate movements, at the land side, or information about their movements per hour at the sea side of the terminal. 

Possible APIs:

- **Access/Wait time**: Estimated period of time that trucks have to queue before they can enter into a terminal.
  - Request parameters: port name, port UN/LOCODE, terminal.
  - Data included in the response: number of minutes.
  - [catalog](catalog/catalog-AccessTime.md)
- **Goods/Containers entrance/exit of Terminals**: Number of units (containers, freight cars,...) that enter or leave a terminal per hour during the present day.
  - Request parameters: port name, port UN/LOCODE, terminal, direction of the flow of the units.
  - Data included in the response: number of units, direction of the flow, hour.
  - [catalog](catalog/catalog-GateMovements.md)
- **Vessel Loading/Unloading**: Number of containers loaded or unloaded from a vessel per hour during the present day.
  - Request parameters: port name, port UN/LOCODE, terminal, direction of the flow of the equipments (loading or unloading).
  - Data included in the response: number of units, direction of the flow, hour.
  - [catalog](catalog/catalog-LadingUnloading.md)

### News 
![Newspaper](https://github.githubassets.com/images/icons/emoji/unicode/1f4f0.png?v8)

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

![Notices](https://github.com/portdebarcelona/OpenInfoAPI-Ports/blob/develop/docs/images/Notices.png?raw=true)

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

![Bookmark tabs](https://github.githubassets.com/images/icons/emoji/unicode/1f4d1.png?v8)

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
- **Cargo fees**: List of the port rates and fees associated to the flow of goods at a specific port.
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
![Calendar](https://github.githubassets.com/images/icons/emoji/unicode/1f4c6.png?v8)

The companies and administrations that operate in a port are not always operational. The hours of service and attention to the public of these companies may vary and may even be subject to specific festivities. And this knowledge can be of great help when a particular operation must be carried out through our Port.

Information about working days, weekend days, and list of public holidays from the requested date period and port.

Possible APIs:

- **Port calendar**: Query about the companies that will work on a specific period of time.
  - Request parameters: port name, port UN/LOCODE, name of the company, activity, selected period of time.
  - Data included in the response: json with the name of the company, day of the selected period, opening hours on that day.
  - [catalog](catalog/catalog-Calendar.md)


### Port Directory
![Office](https://github.githubassets.com/images/icons/emoji/unicode/1f3e2.png?v8)



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


