# TODO list proposals

Proposals of changes, extensions, improvements, corrections.

## Proposal of changes of OpenAPI specification

- Add ws 'Info' to all services. Returns description, parameters and outputs
- In Liner Services, add **types of Cargo Services** (containers, roro, bulk, ...)
- **Time is in utc?** always? we would have to publish localdatetime also?
- **Berths**
  - Add terminalName ¿?
- Add **shipTypes**, list of codes and descriptions o ship types (see Annex VI from DIRECTIVE 2009/42/EC OF THE EUROPEAN PARLIAMENT AND OF THE COUNCIL of 6 May 2009)

- **typesOfCargo**: proposal: [] { "code": "32", "description": "40 ft freight units"}, ...] instead of 	[ "32", ...] (without description)
- **ApproachInstructions**: Simplify with a URL

## Proposal of new OIAP services

- **Notify me when arrives a ship**
- **TerminalCode** is used in accessWaitTime. Where we provide a list of TerminalCodes?

## Implement OIAP webservices at Port of Barcelona

- **Implemented**:
  - **Ship Calls**
  - **Liner Services**
  - **Port Infrastructures**
    - portGates
    - berths
    - railTerminals
  - **Port Procedures**
    - customsClearanceProcedures
    - borderInspectionProcedures
    - vgmProcedures
    - qualityCertificationProcedures
    - partnerActivities
    - pickupProcedures
    - deliveryProcedures
    - approachInstructions
  - **Statistics**
    - typesOfCargoList
    - commoditiesList
  - **Environment-Weather**
  - **Environment-Sea State**
  - **Environment-Pollution**
  - **Rail Transport**
  - **Vehicle Traffic**
  - **Terminal Performance**
  - **News**
  - **Notices**
  - **Rates and Fees**
  - **Port Services**
    - serviceTypes
  - **Port Calendar**
    - holidays
    - holidayTypes
  - **Port Directories**
    - companyActivities
  
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
  - accessWaitTime ()
  - landsideThroughput

## Diffusion

- Publish web with gitpages
- Open Twitter account
- Produce information pills
