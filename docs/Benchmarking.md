# Benchmarking
some words of introduction about benchmarking ....

## ShipCalls
There are many implementations about shipcalls. Ens hem fixat amb alguns dels principals.
### Definitions and Implementations

**Definitions**: About definition and content of ship calls we remark:
- [BERMAN message in Puertos Del Estado](http://www.puertos.es/Documents/BERMAN%204.1.2%20v1.0.pdf) and also [UNCEFACT](https://service.unece.org/trade/untdid/latest/trmd/berman_c.htm). Main standard used to request a ship call sent by shipagents to Port Authorities.- [DCSA Just in Time Port Call](https://dcsa.org/initiatives/just-in-time-port-call/). Proposal procedure with aim to synchronize ship calls with port operations. And furthermore wants to reduce pollution at port areas.- [SMDG Vessel schedules](https://newsmdg.de/documents/edifact-migs-message-implementation-guidelines/vessel-schedules/). EDIFACT Messsage Implementation Guideline for vessel arrival/departures schedules (VESDEP), alternative to BERMAN message. 
### Discussion
A ship call is defined by these main concepts: IMO ship identification number and name of ship, Port of origin, Port of call, Berth, date and time expected (or actual) of arrival, date and time expected (or actual) of departure , and Port of Destination. The type of ship is also included (e.g.: container ships, tankers, bulk carriers, ferries, cruise ships, car carriers, Ropax).

The EDIFACT messages mentioned include much more information on the scales of the ships, their characteristics, their cargo and the services required (mooring, towing, pilotage, waste collection). In this proposal, only the 'core' part of the standardized messages will be used, as stated in the previous paragraph.

Introduir el paràgraf per enviar-lo al [CatalogIntroduction/Shipcalls](CatalogIntroduction.md)



#### Content
Resum del contingut principl i link catalog/....
#### Implementation
Resum ... link al catalog/...

===

## Realtime weather
adfa
## Weather Forecast--- 

## Sea state
asdfa
...

## Pollution
asdf
## Traffic Status 
asdf
## Rail Transport Calls
asdf
## Rail Transport Services (o liners)
adsf
## Liner Services
asdf

## Terminal Trailer Queues (Gate Congestion)
Tiempos de acceso

## Container Gate In/Out
ref a Codeocos

## Container Ship (un)loading operations
ref Coarris
## Inspecciones sobre la mercancía- PIF- escáner
## News

## Notices

# Benchmarking of services by Port

## Port of Antwerp (NxtPort)

Antwerp port facilitate services through NxtPort plataform. See at https://www.nxtport.com/en/market/our-marketplace/marketplace#live
- Arrival at Exit: Send the Charge Report (IE507) to Customs for export containers known in the E-balie application
- Bulkchain: Bulkchain digitises the non-commercial communication between all supply chain members in the Breakbulk & project cargo sector.
- CCRM: Request or get notified about the Customs status of a container and know when it is allowed to leave the terminal.
- Certified Pick up: An innovative solution for releasing containers in the Port of Antwerp.
- e-Balie+ Notifications: Receive status updates for cargo reported through e-Balie/e-Desk
- Export_Manifest: Send an automated manifest when vessels with export cargo leave the port
- Import Consignment: Re-use the cargo information digitally
- Port Directory: Up to date contact information by integrating your systems with the yellow pages of the port community
- Portcall+: Precise and real-time information on the movement of vessels
- PortStays: Get an overview of all active sea-going vessels in Antwerp
- Push Barges Location: Push Barges Location
- Qronoport: Get visual insights into what other stakeholders have planned on liquid bulk vessels you have to work on, improving planning and reduce lost time.
- Terminal Events: Enrich your view on your container voyage by obtaining the terminal gate in and out moves
- Tresco Location: Lat 51.297273 / Lon 4.268129 may not ring a bell, 'Deurganckdok' probably does
- UN/Locode: Use the UN/LOCODE dataset with ease in your applications
- VGM: Method 1: Request the weight of an export container (SOLAS method I)
- VGM: Tare Weight: Request the tare weight of any container to meet the SOLAS VGM (method 2) requirements.
- VisiGIP: Follow your container through the customs process
- VisuRIS: Visualise the transport and traffic-aspects on inland waterways
- Green Lights: Check the different release steps of your container in the import process
- Next Mode of Transport: Announce the NMoT of your container to the terminal
  
## Port of Busan 

Port of Busan explain their services at https://www.data.go.kr/en/bbs/ntc/selectNotice.do?originId=NOTICE_0000000002021

We will inform you of the disposal of API related to Busan Port Authority. 1) Provider: Busan Port Authority 2) Target service (15 types of API)-Busan Port RFID vehicle access data-Pier information-Terminal code-Integrated cargo report information (disembarkation report)- Ship specification information-Ship control information-Ship entry/departure information-Loading list prior report container weight information inquiry-Terminal shipping code-

Terminal bus code-Terminal container device information-Terminal loading and unloading plan information-Container status information-Unloaded container list-Overseas Port code 3) Reason for disposal: System maintenance has been steadily performed since 2011 to provide public data, but it is decided to dispose of the existing system due to the fact that it is impossible to maintain the existing system such as the end of the flash service 4) Person in charge: Information system manager of Busan Port Corporation 3145

## The Maritime and Port Authority of Singapore (MPA)

The MPA signed a memorandum of understanding (MoU) with five international partners today, to develop and adopt common data standards and Application Programming Interface (API) specifications, which will facilitate data exchange for port and maritime services transactions. These partners are CargoSmart (solution provider for the Global Shipping Business Network), GTD Solutions (representing TradeLens), GeTS and PSA International (jointly representing CALISTA), and the Port of Rotterdam Authority.

Annex A: Areas of cooperation covered by the MoU on common data standards and Application Programming Interface (API) specifications

(a) Generate awareness in the maritime industry about the importance of common data standards and common API specifications across international maritime jurisdictions and platforms;

(b) Sharing of information and best practices in the maritime industry pertaining to the harmonisation of data standards across international maritime jurisdictions and platforms;

(c) Development of common data standards and common API specifications to facilitate data exchange for business activities and transactions;

(d) Adoption of common data standards and API specifications to facilitate data exchange for business activities and transactions;

(e) Adoption of open data sharing by Parties with existing and/or future relevant platforms and databases for efficient flow of information across global maritime transport chains;

(f) Provision of resources, support, capabilities, expertise and setting up of jointentities, whenever applicable, to encourage research and development, test-bedding and adoption of solutions and technologies to facilitate wider adoption of the common API specifications in the maritime industry.

# Terminals Services and others

## Long Beach Container Terminal

Long Beach Container Terminal https://www.globenewswire.com/en/news-release/2019/07/30/1893980/0/en/Long-Beach-Container-Terminal-develops-Application-Programming-Interfaces.html

Planificador del transporte de Hutchison Ports (UK) https://hutchisonports.com/media/stories/paris-api-the-next-generation-in-transport-planning-and-optimisation/ parisoptimalplanning.com https://api.parisoptimalplanning.com/guide/introduction/1

## TradeLens API

And this here is one of the best API for supply chain that is based on blockchain and will provide you with the info on the timely location of shipments and their characteristics (temperature, transit passages, etc). https://docs.tradelens.com/reference/api_documentation/

## IPCSA – network of trusted networks (NoTN) 

https://notn.ipcsa.international/

- Portcall: Receive a real time overview of the time of arrival and departure of vessels from ports across the world in order to support your users planning of port operations and cargo movement. https://notn.ipcsa.international/notn-market/portcalls-info
- Cargo status: The PCS client accesses this service in order to get track and trace data of an equipment loaded or discharged at a certain port (shipment). https://notn.ipcsa.international/en/notn-market/cargo-status

## APM Terminals https://www.apmterminals.com/en/tools/api

- Import Availability
- Export Booking Enquiry
- Vessel Schedule
- Container Event History
- Truck Appointments
- Empty Container Returns
