# TODO list proposals

Proposals of changes, extensions, improvements, corrections.

# About OpenAPI specification

- In Liner Services, add types of Cargo Services (containers, roro, bulk, ...)
- holidays:
  - which reference we use?
  - add holidayName in yml
- add holidayTypes = [ national holiday, other secular holiday, religious holiday, regional holiday local holiday ] --> DONE!
- Time is in utc? always? we have to publish localdatetime?
- **Berths**
  - Flatten? "berthCoordinates": { "latitude": 41.299813, "longitude": 2.156614 }
  - Add terminalName ¿?
- **serviceTypes**: Change:
  - [ "serviceType": "Stevedoring & Lashing"  }, ... ]  to:
  - [ "Stevedoring & Lashing",  ]
- **portServices** maybe must be **shipServices** ??  --> DONE!
- Add **shipTypes**, list of codes and descriptions o ship types (see Annex VI from DIRECTIVE 2009/42/EC OF THE EUROPEAN PARLIAMENT AND OF THE COUNCIL of 6 May 2009)
- **customsClearanceProcedures**, **borderInspectionProcedures**, **qualityCertificationProcedures** must to be a list of dicts or a unique dict?
- **containerTare** must to be a list of dicts or a unique dict?
  - queryParams": {  "portCode": "ABCU1234567" } must be { "containerNumber" : "ABCU1234567" }

# Diffusion

- Publish web with gitpages
- Open Twitter account
- Produce information pills

