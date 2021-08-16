# Introduction to the catalog of APIs
This catalog enumerates a list of APIs with information about ports that can be useful for the logistic activities and also for the citiens that want to know more about ports.

## Categories

Use of **Categories**. Many concepts are common in all ports (e.g., port services). It is advisable to use a category field that would allow better filtering and precise referencing.

### Ships Calls
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
  - Request parameters: port name, port mouth,...
  - Data included in the response: fixed bridges and other structures over navegable waters, identification parameters of those structures, latitude/longitude,...
  - [catalog](catalog/catalog-MarineAids.md)

### Port Procedures (Work in progress)
Certain operations require some procedure instructions and these procedures should be published and accessible to several applications. 

Here are some examples of APIs that can facilitate information of some of these procedures:
- **Approach instructions** (PENDING)
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
 
- **Customs Inspections**

  Customs can perform their physical inspections inside the cargo terminals, at the terminal yard or in a warehouse, but they can also inspect containers, platforms or trucks using a non-intrusive technology as an X-ray scanner. Operators need to know which units have been selected to be inspected by Customs, to know if the inspection has been carried out and whether the goods have been cleared. 
  
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
    - Data included in the response: unit of cargo selected for inspection (true/false), border inspection service (phytosanitary, veterinary, pharmacy, health,...), type of inspection (identity,...), place of the inspection (container yard, border inspection post, pre delivery inspection (PDI),...), status (pending/carried out/cleared,...),...
    - [catalog](catalog/catalog-BorderInspections.md)   

- **Port Calendar** (PENDING) 
- **Container release (Container pick-up from the terminal)** (PENDING)
- **Container Acceptance (Conteiner delivery to the terminal)** (PENDING)
- **Efficiency Network Certificate** (PENDING)

### Statistics
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

### Weather
Introduction to meteorological data. See [Free Weather APIS to access global weather data](https://rapidapi.com/blog/access-global-weather-data-with-these-weather-apis/), [wheatherapi.com](https://www.weatherapi.com/docs/#apis-realtime)

#### Realtime weather

- **WeatherTemperature**:
- **WeatherPressure**:
- **WeatherWindSpeed**:
- **WeatherWindDirection**:
- ...
#### Weather Forecast

- **WeatherForecast**: 
- **WeatherTemperatureForecast**:
#### Weather Alerts
- ...
### Sea State
Altura y dirección olas
Previsión oleaje

### Pollution
Publicación en tiempo real [wheather api](https://www.weatherapi.com/docs/#intro-aqi)

- Estimaciones de CO2 emitido en función de las operativas
- Previsión episodios
- Descargas graneles
- **Water quality** 

### Vehicle Traffic
Entradas y salidas de vehículos del recinto portuario

### Train services (o liners)

### Train information

- **Train Exits**
- **Train Arrivals**

### Terminals
- Access/Wait time
- Goods/Containers entrance/exit of Terminals
- Vessel Loading/Unloading

### News
[see 'NewsArticle' at schema.org](https://schema.org/NewsArticle)

### Notices
Often, Port Authorities have to publish some notices (meteorological alerts, port procedures, etc ). Normally these notices are sent by mail and sms, and published in the web. But also is necessary to publish in web services.

Some notices are intended for the port community, and others are intended for the general public. Also, each notice is of interest to some subgroups of the port community, such as ship agents, shipping companies, transport companies, stevedore,  concessionaire, etc.

### Port rates and fees Info

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

### Port Services Info

Information about services that are offered by a port. Eg: bunkering, marpol, mooring, pilots, tugs,... (TODO buscar a la web de l'APB)

### Port Calendar

Information about workdays, local holidays, ... 

### Port Directory

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

**Info Open APIs should**:
- Publish kind of services that offer (catalog of services)
- Allow filter companies depending on services that offer
- Alow get information contact of a company (Name, email, phone, address, icon, etc)

[see 'Organization' in schema.org](https://schema.org/Organization)
[evaluate 'Offer' in scehma.org](https://schema.org/Offer)
