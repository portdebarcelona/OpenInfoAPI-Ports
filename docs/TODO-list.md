# TODO list proposals

Proposals of changes, extensions, improvements, corrections.

## Proposal of changes of OpenAPI specification

- Add ws '**Info**' to all services. Returns description, parameters and outputs
- In Liner Services, add **types of Cargo Services** (containers, roro, bulk, ...)
- **Time is in utc?** always? we would have to publish localdatetime also?
- **Berths**
  - Add terminalName ¿?
- Add **shipTypes**, list of codes and descriptions o ship types (see Annex VI from DIRECTIVE 2009/42/EC OF THE EUROPEAN PARLIAMENT AND OF THE COUNCIL of 6 May 2009)
- **typesOfCargo**: proposal: [] { "code": "32", "description": "40 ft freight units"}, ...] instead of 	[ "32", ...] (without description)
- **accessWaitTime**:
  - Include datetime of data reading in each terminal
  - Question: terminalCode follows some rule? 'ESBCN-00042'

## Proposal of new OIAP services
- **Info** or **/**: Webservice that return:
  - Version of oiap
  - List and description of services oiap implemented
- **Notify me when arrives a ship**
- **TerminalCode** is used in accessWaitTime. Must we provide a list of TerminalCodes with access time data?

## Implement OIAP webservices at Port of Barcelona

- **Implemented**:
  - *Ship Calls* group
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
  - shipsInPort
  - shipsArrivals
  - shipsDepartures
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
