# Introduction to Info Open API catalog of Ports
About ports ... and info

## Categories

Use of **Enumerations**. Many concepts are common in all ports (for instance: port services). It is advisable to use an enumeration field that would allow better filtering and precise references
### Ship Calls
Introduction to ship calls.

Proposals:
- **Ships Arrival Forecasts**. Forecast o ships that will arrive at a port. Data: IMO number, ship name, ETA (Estimated time of arrival), etc [catalog](catalog/catalog-ShipsArrivalForecasts.md)
- **Vessels in port**. Vessels that are moored in the port. Data: IMO number, ship name, ATA (Actual time of arrival), ETD (Estimated Time of Departure), mooring Quay, etc [catalog](catalog/catalog-VesselsInPort.md)
- **Ship Exits**:
- **Ship Arrivals**: 
- **Ships Aproximation Manouvres**: Aproximation manouvres of ships to the port.
- **Ferries Arrivals**: [catalog](catalog/catalog-FerriesArrivals.md)
- **Ferries Departures**: [catalog](catalog/catalog-FerriesDepartures.md)
- **Cruises Calls**: [catalog](catalog/catalog-CruisesCalls.md)

**Benchmarking**: [veure](Benchmarking.md#ShipCalls)
### Liner Services
An important offer of a Port its related to foreland connections. So that, a port must publish a list with which ports have sea conection. This information should contain:
- Liner Service Name
- Shipowner
- Periodicity
- List of linked ports
- TEU weekly
### Ports Infrastructure
Information about port insfrastructure:
- Latitude/Longitud
- Land area
- Berths (length, depths, loading capacities, contact information)
- Terrestrial Gates
- Terminals: 
  - Ferris terminals
  - Cruiser terminals
  - Container terminals
  - Vehicle Terminals
  - Bulk Terminals
- Marine Aids to Navigation

### Port Procedures
All ports have procedure instructions for certain types of operations. These procedures must be published and accessible to applications. Here sompe examples:
- Approach instructions
- VGM (Verified Gross Mass)
- Customs Inspections:
  - Inspection in Terminal
  - Non intrusive Inspection
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
All the port have statistic information about activity. Usually are published annually, monthly, quarterly. Relevant data of a port are:
- Number ship calls
- Tones loaded/unloaded
- Numer of containers
- Vehicles loaded/unloaded
- Passengers embarkded/disembarked
- Liquid bulks loaded/unloaded
- Solid bulks loaded/unloaded
- Economic concepts
- etc.

### Weather
Introduction to meteo. See [Free Weather APIS to access global weather data](https://rapidapi.com/blog/access-global-weather-data-with-these-weather-apis/), [wheatherapi.com](https://www.weatherapi.com/docs/#apis-realtime)

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
Often, Port Authority have to publish some notices (meteorological alerts, port procedures, etc ). Normally these notices are sent by mail and sms, adn published in the web. But also is necessary to publish in webservices.

Some notices are intended to port community, and other are intended to general public. Also each notice is of interest of some subgroups of port community, such as: shipagents, shipping companies, transport companies, stevedors,  concessionaire, etc.

### Port fees Info

Information about official fees of port services. Eg: navigation adis, goods (T3)... (TODO buscar a la web)

### Port Services Info

Information about services that are offered by a port. Eg: bunkering, marpol, mooring, pilots, tugs,... (TODO buscar a la web de l'APB)

### Port Calendar

Information about workdays, local holidays, ... 

### Port Directory

Logistic services of a port are ofered through specialized companies. A port should publish companies, contact information, and services offered by stakeholders of a port. Mainly have to procure two APIs: one for creating and updating contact data, and another API to publish contact information. This is a classifications of port services that have to be used to tag contact info:

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
- Allow filter companies depending services that offer
- Alow get information contact of a company (Name, email, phone, address, icon, etc)

[see 'Organization' in schema.org](https://schema.org/Organization)
[evaluate 'Offer' in scehma.org](https://schema.org/Offer)
