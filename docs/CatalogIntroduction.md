# Introduction to Info Open API catalog of Ports
About ports ... and info

## Categories

Use of **Enumerations**. Many concepts are common in all port (for instance: port services). Its advisable to use enumeration field that would allow better filtering and precise references
### Ship Calls
Introduction to ship calls.
- **Ship Arrivals Forecast**. Forecast o ships that will arrive to a port. Data: IMO number, ship name, ETA (Estimated time of arrival), etc [catalog](catalog/catalog-ShipsArrivalForecasts.md)
- **Vessels in port**. Vessels that are moored in the port. Data: IMO number, ship name, ATA (Actual time of arrival), ETD (Estimared Time of Departure), mooring Quay, etc [catalog](catalog/catalog-VesselsInPort.md)
- **Ship Departures**:
- **Ship Arrivals**: 
- **Ship Aproximation Manouvres**: Aproximation manouvres of ships to the port.
- **Ferries Arrivals**: [catalog](catalog/catalog-FerrysArrivals.md)
- **Ferries Departures**: [catalog](catalog/catalog-FerryDepartures.md)
- **Cruise Calls**: [catalog](catalog/catalog-CruisersCalls.md)

### Liner Services
An important offer of a Port its related to foreland connections. So that, a port must publish a list with which ports have sea conection. This information should contain:
- Liner Service Name
- Shipowner
- Periodicity
- List of ports
### Port Infrastructure
Information about port insfrastructure:
- Latitude/Longitud
- Land area
- Berths (length, depth, loading capacities, contact information)
- Terrestrial Gates
- Terminals: 
  - Ferry terminals
  - Cruise terminals
  - Container terminals
  - Vehicle Terminals

### Port Procedures
All ports have procedure instructions for certain types of operations. These procedures must be published and accessible to applications. Here sompe examples:
- Approach instructions
- VLM,
- etc

### Statistics
All the port have statistic information about activity. Usually are published annually, monthly, quarterly. Relevant statistical data of a port are:
- Number of ship calls
- Tones loaded/unloaded
- Number of containers
- Vehicles loaded/unloaded
- Passengers embarkded/disembarked
- Liquid bulk loaded/unloaded
- Solid bulk loaded/unloaded
- etc

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
- Wave height and direction
- Swell direction
- Waves forecast

### Contamination
Contamination (real-time) [wheather api](https://www.weatherapi.com/docs/#intro-aqi)

- Estimation of CO2 emitted
- Forecast of pollution episodes
- Bulk unloading 

### Vehicle Traffic
Vehicle entrance or exit of the zone of the service of the Port

### Train services (o liners)

### Train information

- **Train Departures**
- **Train Arrivals**

### Port Terminals
- Terminal access time
- Goods entry or exit
- Vessel loading/unloading

### Inspections of goods
- Border Inspection Post
- Scanner (non intrusive inspection)

### News
[see 'NewsArticle' at schema.org](https://schema.org/NewsArticle)

### Notices
Often, Port Authority have to publish some notices (meteorological alerts, port procedures, etc ). Normally these notices are sent by mail and sms, adn published in the web. But also is necessary to publish in webservices.

Some notices are intended to port community, and other are intended to general public. Also each notice is of interest of some subgroups of port community, such as: shipagents, shipping companies, transport companies, stevedors,  concessionaire, etc.

### Port companies
Direcciones y datos de contacto

### Port Directory
Logistic services of a port are ofered through specialized companies. A port should publish companies, contact information, and services offered by stakeholders of a port. This is a classifications of port services:
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
