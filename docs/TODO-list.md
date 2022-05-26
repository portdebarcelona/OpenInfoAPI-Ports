# TODO list proposals

Proposals of changes, extensions, improvements, corrections.

## Modificacions of OpenAPI specification

- In Liner Services, add **types of Cargo Services** (containers, roro, bulk, ...)
- **Time is in utc?** always? we would have to publish localdatetime also?
- **Berths**
  - Add terminalName ¿?
- Add **shipTypes**, list of codes and descriptions o ship types (see Annex VI from DIRECTIVE 2009/42/EC OF THE EUROPEAN PARLIAMENT AND OF THE COUNCIL of 6 May 2009)

- **typesOfCargo**: proposal: [] { "code": "32", "description": "40 ft freight units"}, ...] instead of 	[ "32", ...] (without description)
- **ApproachInstructions**: Simplify with a URL

## News OIAP services

- **Notify me when arrives a ship**
- **TerminalCode** is used in accessWaitTime. Where we provide a list of TerminalCodes?

## Implement OIAP webservices at Port of Barcelona

- Done:
  - berths
  - railTerminals
  - portGates
  - typesOfCargoList
  - commoditiesList
  - serviceTypes
  - holidays
  - holidayTypes
  - companiesActivities

- Working on:
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
  - customsClearanceProcedures
  - borderInspectionProcedures
  - vgmProcedures
  - qualityCertificationProcedures
  - qualityCertifiedPartners
  - partnerActivities
  - pickupDeliveryProcedures
  - approachInstructions

## Diffusion

- Publish web with gitpages
- Open Twitter account
- Produce information pills
