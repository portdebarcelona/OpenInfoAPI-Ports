# Semantic approach

There are some basic concepts that must be reviewed before defining our approach.
There is an introduction to some of these concepts [here](./semantic.md).   

## Top-down approach
- A top-down approach will be followed to define the data model for "Open Info API para puertos", following this steps:
  1. Identification of the **domains** that will be covered in the project.
  2. Identification of several **APIs** for each domain.
  3. Possible **input and output parameters** of those APIs.
  4. From parameters to **entities and their attributes**.
  5. **Data model** specification: entities and attributes that are properties or relationships.

## Domains
- Although it is a list that can always be expanded, the following domains appear in this initial version:
  1. **Ships Calls**. Information about actual or planned ships calls at a specific port. Including scheduled arrivals and departures.
  2. **Liner Services**. Information of liner services, carriers involved and ports serviced. 
  3. **Port Infrastructure**. Basic data of the infrastructure of a port, its land and sea accesses, its terminals and its railway infrastructure. 
  4. **Port Procedures**. Links to the websites where all port procedures of a port are described.
  5. **Statistics**. Traffic and economic statistics of a port.
  6. **Environment** This domain covers weather, sea state and pollution information associated to a port.
  7. **Rail Transport** Information about rail transport in ports, including their rail connections, linked railway terminals, train arrivals and departures and information about all the actors involved in this type of transport.
  8. **Vehicle Traffic Monitoring** Information about the number of vehicles entering or leaving a port area.
  9. **Terminals** Information about terminal performance, including the number of cargo units that enter or leave from a terminal per hour, the number of cargo units loaded or unloaded per hour from vessels or the wait time of trucks to enter to a terminal.
  10. **News** News from a port, including the possibility to subscribe to a service of news. 
  11. **Notices** Notices of interest from a port, including the possibility to subscribe to a service of port notices. 
  12. **Port Rates and Fees** Link to the web page where port rates and fees of a port are published. 
  13. **Port Services** Information about services that are offered by a port and which vessels can order those services. E.g.: bunkering, marpol, mooring, pilots, tugs,...
  14. **Port Calendar** Information about working days, weekend days, and list of public holidays from the requested date period and port.
  15. **Port Directory** Information about companies and administrations that operate in a port.

## Catalog of APIs
- [Here](./CatalogIntroduction.md) there are some examples of possible APIs.

## APIs' Input and Output Parameters
- Within the [catalog of APIs](./CatalogIntroduction.md), accompaining each example of API, there is also a list with its input and output parameters.

## Entities and attributes
- The parameters identified in each API can be classified as entities or atributtes of some entities.