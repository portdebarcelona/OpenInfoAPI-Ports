# TODO list proposals

Proposals of changes, extensions, improvements, corrections.

## Proposal of changes of OpenAPI specification

- Add to'**Info**'  parameters.
- In Liner Services, add **types of Cargo Services** (containers, roro, bulk, ...)
- **Time is in utc?** always? 
  - we would have to publish localdatetime also?
  - we should distinguish wtih name o attributtes (utcDate?, localDate?)
- **Berths**
  - Add terminalName ¿?
- Add **shipTypes** webservice, list of codes and descriptions o ship types (see Annex VI from DIRECTIVE 2009/42/EC OF THE EUROPEAN PARLIAMENT AND OF THE COUNCIL of 6 May 2009)
- **typesOfCargo**: proposal: [] { "code": "32", "description": "40 ft freight units"}, ...] instead of 	[ "32", ...] (without description)
- **accessWaitTime**:
  - Include datetime of data reading in each terminal: 'recordTime'
  - Question: terminalCode follows some rule? 'ESBCN-00042'>> IMO Code
  - Needed a webservice that return a list of terminalCodes that have info of accessWaitTime

- **trainArrivals**:
  - add field "name" in station/terminal Departure/Destination

- **shipsArrivals**:
  - Fix 'shipArrivals' in returns (singular vs plural)
  - convert shipTypes to DIRECTIVE 2009/42/EC 

- **shipsDepartures**:
  - Fix 'shipsDepartures' in returns (singular vs plural)

- **landsideThroughput**:
  - Add field 'meanOfTransport? [ 'TRUCK', 'TRAIN' ]
  - Add field 'Units'?  [ 'TONES', 'TEUS', ... ] ?
  - Add field 'Date'? ex: "2020-05-30"
  - Modify 'hourReported'? '18-19' instead of '18' . Check ISO way
  - Add query parameters:
    - Date. Default: 'today'
    - Hour?
  - Modify returns: one item info for each hour reported of the day (instead of last hour)
  - Needed a webservice that return a list of terminalCodes that have info of landsideThroughput

- add **passengerTerminals** in tag PortInfrastructure
  - codeterm
  - shortname (optional)
  - fullname
  - coords (optional)
  - kindof (ferris/cruisers)

- **portInfrastructure**: 
  - Must be a dict not a list of dicts!!??
  - Return strings instead of integers (landarea, berths, ..warehousing), including units "131 ha"
  - More fields? see memory. Proposal:
    - portName : Barcelona
    - portCode : ESBCN
    - portCoordinates :
      - latitude: 41,21
      - longitude : 2,10
    - landArea: 1113,2 ha
    - Wharves and berths: 23.183 km
    - Ro-ro ramps 30
    - Draught up to 16 m
    - Warehousing
      - Covered 203,304 m2
      - Uncovered 5,023,964 m2
    - ? Dry dock?
    - ? Entrance ?

- **portRatesAndFees** Must be a Dict instead of a list of dicts?
- **trafficFlowObserved**. Revise queryParameters:
  - portGate must be gateName (or a list or gates?)
  - vehicleTypes must be a list. eg [ 'Truck', 'Van']
  - Delete external flowDirection
- **vehicleTypes** webservice needed for trafficFlowObserved
  - Proposal: [ 'Any', 'Truck', 'Car', 'Bus', 'Van', 'Motorcycle' ]
- **All webservices**:
  - Add in metadata 'Info', 'Units' (ex minutes of waittime) ?

## Proposal of new OIAP services
- **Info** or **/**: Webservice that return:
  - Version of oiap
  - List and description of services oiap implemented
- **Notify me when arrives a ship**
- **TerminalCode** is used in accessWaitTime. Must we provide a list of TerminalCodes with access time data?

## Implement OIAP webservices at Port of Barcelona

- **Implemented**:
  - *Ship Calls* group
    - **shipsInPort** (need function that returns data of berth and LOCODEPORTORIGEN)
    - **shipsArrivals**
    - **shipsDepartures**
  - *Liner Services* group
  - *Port Infrastructures* group
    - **portGates**
    - **berths**
    - **railTerminals**
  - *Port Procedures* group
    - **customsClearanceProcedures**
    - **borderInspectionProcedures**
    - **vgmProcedures**
    - **qualityCertificationProcedures**
    - **partnerActivities**
    - **pickupProcedures**
    - **deliveryProcedures**
    - **approachInstructions**
  - *Statistics* group
    - **typesOfCargoList**
    - **commoditiesList**
  - *Environment-Weather* group
  - *Environment-Sea State* group
  - *Environment-Pollution* group
  - *Rail Transport* group
    - **trainArrivals**
    - **trainDepartures**
  - *Vehicle Traffic* group
  - *Terminal Performance* group
    - **accessWaitTime**
  - *News* group
  - *Notices* group
  - *Rates and Fees* group
  - *Port Services* group
    - **serviceTypes**
  - *Port Calendar* group
    - **holidays**
    - **holidayTypes**
  - *Port Directories*group
    - **companyActivities**
  
- **Working on**:
  - shipsScheduled
  - shipsAproximation
  - ferriesArrivals
  - ferriesDepartures
  - cruiseCalls
  - linerServices
  - linkedPorts
  - linerCarriers
  - portTerminals
  - landsideThroughput

## Diffusion

- Publish web with gitpages
- Open Twitter account
- Produce information pills
