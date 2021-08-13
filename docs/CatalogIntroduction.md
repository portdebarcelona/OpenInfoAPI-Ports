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
  - The request parameters will be: liner service name, shipowner, type of cargo,... 
   - The data included in the response: liner service name, shipowner, type of cargo, periodicity, list of linked ports, capacity (TEU weekly),...
   - [catalog](catalog/catalog-LinerServices.md)

### Port Infrastructure
Information about port infrastructure (PENDING)

Possible APIs:
- **Port infrastructure**
  - The request parameters will be: port name,... 
   - The data included in the response: latitude/longitud, land area, berths (length, depth, loading capacities, contact information),...
   - [catalog](catalog/catalog-PortInfrastructure.md)
- **Port gates**
  - The request parameters will be: none. 
   - The data included in the response: gate name, latitude/longitud, allowed vehicles, maximun width, maximum height, opening hours,...
   - [catalog](catalog/catalog-PortGates.md)
- **Port terminals**
  - The request parameters will be: none. 
   - The data included in the response: terminal name, type of terminal (ferry, cruise, container, multipurpose, vehicle, Bulk cargo,...), gate latitude/longitud, allowed vehicles, maximun width, maximum height, opening hours,...
   - [catalog](catalog/catalog-PortTerminals.md)
- **Marine Aids to Navigation**
  - The request parameters will be: (PENDING) 
   - The data included in the response: (PENDING)
   - [catalog](catalog/catalog-MarineAids.md)

### Port Procedures
All ports have procedure instructions for certain types of operations. These procedures must be published and accessible to applications. Here are some examples:
- Approach instructions
- VGM (Verified Gross Mass)
- Customs Inspections:
  - Inspection in Terminal
  - Non-intrusive Inspection
- Border Inspection Post
- Port Calendar 
- Container release (Recogida de contenedores en terminal)
- Container Acceptance (Entrega de contenedores en terminal)
- Efficiency Network Certificate

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
