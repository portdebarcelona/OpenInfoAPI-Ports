# OpenInfoAPI-Ports content
- [OpenInfoAPI-Ports content](#openinfoapi-ports-content)
  - [About OpenInfoAPI-Ports](#about-openinfoapi-ports)
  - [Introduction to idea Open Info API for Ports](#introduction-to-idea-open-info-api-for-ports)
  - [Deliverables](#deliverables)
  - [Project Plan](#project-plan)
  - [Changelog](#changelog)
  - [Web Page](#web-page)
  - [About Ports 4.0](#about-ports-40)
    
## About OpenInfoAPI-Ports
- IDEA awarded at [Ports 4.0 call](https://ports40.es/static/program_idea) on April 9, 2021.
- [Ports 4.0 decision](docs/annexes/IDEAS-RESOLUCION-PROVISIONAL-CONCESION-DE-AYUDAS_signed.pdf)
- [More detailed presentation](docs/Presentation.md)
## Introduction to idea Open Info API for Ports
All the large commercial ports manage a logistics area where goods change their mode of transport, from the seaside (vessels) to the land side (trucks or trains) and vice versa. This activity is specified as:
- Vessels that arrive at port, load and unload their cargo (usually in containers/UTIs or as a bulk cargo),
- Port companies that facilitate the access and berthing of the vessel,
- Stevedores who operate the cranes that unload the cargo or equipments from the vessel to the terminal yard or vice versa,
- Trucks that bring or take the goods from the port,
- Trains that are loaded and unloaded and that will carry the goods to or from a location in the hinterland.

But ports often cover a wide area, sometimes close to a city, and their activity has to be sustainable from the economical, social and environmental points of view.

All the activities of the ports are carried out under:
- An intense documentary exchange between the port operators,
- Strict surveillance of the port authorities that verify that the administrative, working, personal or environmental safety conditions are met,
- The need to increase the efficiency of logistics processes, offering more **information services** in real-time,
- The need to **increase the transparency** of what happens in the port, which citizens demand from public administrations.

This project is focused on the last two points:
- Identifying and classifying the information of a port in different domains.
- Defining APIs to show port state.
- And doing it following actual standards:
  - HTTP protocol
  - OAS 3.x Open API Specification
  - API REST
  - JSON: API

## Deliverables

The deliverables of this idea will be a **catalog of information** that the ports can use and that will contain the definition of information types and their attributes. All this is defined in OpenAPI with its description and examples published on GitHub.

In this six months plan, deliverables will be:

- Creation of **Github repository** or similar: [this repository](https://github.com/org/portdebarcelona/InfoOpenAPI-Ports)
- Creation of **Swagger repository** or similar
- Definition of the **types of information**: [see](docs/CatalogIntroduction.md)
- **Attributes** of each type of information: [see](docs/catalog/README.md)
- Selection of a **style guide** for API/JSON: [see](docs/catalog/Pendent.md)
- Definition in **OpenAPI 3.0**.
- **Description and examples** in GitHub.


## Project Plan
This project has an agenda that begins on April 9 and ends on October 9, 2021. Milestones of the work plan are:

| Activity                   | Month 1 | Month 2 | Month 3 | Month 4 | Month 5 | Month 6 |
| -------------------------- | ------- | ------- | ------- | ------- | ------- | ------- |
| Setup of github repository | XXXXXX  |         |         |         |         |         |
| Setup of API repository    | XXXXXX  |         |         |         |         |         |
| Identify information types |         | XXXXXX  | XXXXXX  | XXXXXX  |         |         |
| Define attributes          |         | XXXXXX  | XXXXXX  | XXXXXX  | XXXXXX  |         |
| Define in Open API 3.x     |         |         | XXXXXX  | XXXXXX  | XXXXXX  |         |
| Develop examples           |         |         |         |         | XXXXXX  | XXXXXX  |
| Document in Github         |         | XXXXXX  | XXXXXX  | XXXXXX  | XXXXXX  | XXXXXX  |

## Changelog
Work progress is registered on own page:
- [Work tracking](docs/changelog.md)

## Web Page
Web of this project is built with gitpages: https://portdebarcelona.github.io/OpenInfoAPI-Ports/

## About [Ports 4.0](https://ports40.es/static/ports_40)

The **Ports 4,0** equity fund is the corporate open innovation model adopted by the **Spanish State Port Authorities** to attract, support, and facilitate the application of talent and entrepreneurship to the Spanish public and private ports sector, within the context of 4th industrial revolution.

The main target of the Fund is to actively ***promote and incorporate disruptive or incremental innovation*** as a competitiveness, efficiency, sustainability, security and protection element, in the Spanish public and private logistics-ports sector, to facilitate its transition towards economy 4.0.

Ports 4,0 will ***stimulate the creation or consolidation of a factory of emergent companies*** (Startups), spin-offs, or new business lines, within the technological scope, in existing companies developing innovative market-driven products, services, or processes for the ports logistics sector.
