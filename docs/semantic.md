# Semantics

## Semantics is key for the API standardization
- Semantics, in the context of electronic data exchange, is the unambiguous meaning of
each of the pieces of information to be shared between sender, receiver and any stakeholder
who views or uses the information (CEFACT, documment ECE/TRADE/C/CEFACT/2019/27).
## Some definitions:
### Vocabularies
- A vocabulary define the concepts and relationships used to describe and represent a specific domain.
- Vocabularies are used to classify the terms (entities) that can be used in a particular application, characterize possible relationships, and define possible constraints on using those terms.
- Their role is to help data integration when ambiguities may exist on the terms used.
- Vocabularies can also be used to organize knowledge. 
- W3C offers a large palette of techniques to describe and define different forms of vocabularies in a standard format. These include RDF and RDF Schemas, Simple Knowledge Organization System (SKOS), Web Ontology Language (OWL), and the Rule Interchange Format (RIF). 
- JSON-LD is also suitable for publishing vocabularies because it is useful for both humans and machines.
- There are multiple vocabularies, some of them well established, such as schema.org and the UN/CEFACT vocabulary is valid for trade, transport and administration.
- Schema.org provides the most widely used JSON-LD vocabulary in use today and so is a good guide for what other vocabularies should look like.
- A vocabulary can be published as a file with the reference data models and several files with code lists.
### Code lists
- Some vocabularies are called “codelists”.
- The recommended format for publishing codelists is to use rdf (resource description framework) and a JSON-LD data model.
### Data model / Reference data model / Common Data Models
- A Data Model is an abstract model that organizes information entities and standardizes how they relate to one another and to the real world. The model provides a standard means by which data may be described, categorized and also shared.
- Data Model contains relationships between tables that which addresses cardinality and nullability of the relationships. 
- A Data Model is composed by a set of Entities or Terms, several Attributes, sometimes some Metadata and relationships among them. 
  - Entities:
    - Entities represent a thing. 
    - Entities include a semantic type that describes the type of thing represented by the entity.
    - Some examples of entities are person, company, building, ship, container... 
  - Attributes: 
    - Attributes are properties of entities.
    - Attributes describe the entity they belong to.
    - Attributes also provide information on the interactions between entitiesa (relationship attributes) 
    - Each initiative defines its minimal set of attributes.
    - Some examples of attributes are address, type of ship, temperature,...
  - Metadata:
    - Metadata is data that describes data.
    - Metadata describes what is the functionality provided by an attribute to the user or a system that reads the attribute.
    - Some examples of metadata are date created, accuracy,... 
  - Relationships:

- There are several data models and each one establishes the minimun information for defining their entities and attributes, for example:
  1. The Dublin Core Metadata Initiative (DCMI).
      - The DCMI define their "terms" (entities) with a minimal set of attributes like a:
        - Name
        - Label
        - URI (Uniform Resource Identifier)
        - Definition
        - Type of term
      - And, in DCMI, additional information of the primary entities can be provided with other attributes like:
        - Commentee
        - See
        - Subproperty Of
        - Superclass Of
        - Subclass Of
        - Domain
        - Domain Includes
        - Range
        - Range Includes
        - Member Of
        - Instance Of
        - Equivalent Property
  2. CEFACT
      - CEFACT (see edi3.org) defines its entities with a minimal set of attributes like a:
        - @id
        - @type
        - rdfs:comment
        - rdfs:label
        - uncefact:cefactElementMetadata
          - @id
          - @type
          - uncefact:cefactUNId
          - rdfs:comment
          - uncefact:cefactBusinessProcess
          - 
- Property (Primary entity) like consignment.consignor
- Attributes like: domain or range
- In UN/CEFACT class (Primary entity) and properties belong to a class.
- In a RDM can be defined several versions of the same class intended for use in different contexts.

### Datasets
- Datasets are collections of structured metadata
- There are a set of statements about things, where each statement consists of an element ("attribute") of the entity and a "value" for that element.
### Data dictionaries
- Data dictionaries store and communicate metadata about data in a database, a system, or data used by applications.  Data dictionary contents can vary but typically include some or all of the following:
  - A listing of data objects (names and definitions)
  - Detailed properties of data elements (data type, size, nullability, optionality, indexes)
  - Entity-relationship (ER) and other system-level diagrams
  - Reference data (classification and descriptive domains)
  - Missing data and quality-indicator codes
  - Business rules, such as for validation of a schema or data quality
- This is an example of a data dictionary that can be used for the weather and the pollution domains: http://cfconventions.org/Data/cf-standard-names/46/build/cf-standard-name-table.html
### Linked data
- To make a huge amount of data on the Web available in a standard format, relationships among data should be made available and this collection of interrelated datasets on the Web can also be referred to as Linked Data.
- Integrating facts from several datasets, the application may provide a much better user experience.
- Context:
  - Define context !!!!

### Naming and Design Rules (NDR)
- For the deployment of this IDEA, we propose to use existing vocabularies, when it is possible, and, according to this decission, we can use different vocabularies in our APIs, depending of their Domain. 
- But, not all the Domains covered by our IDEA have a well established vocabulary and we will have to propose our own and therefore we have to establish a Naming and Design Rules.
- Most of the API guidelines include NDR as part of their specification.    

## Open Info API para Puertos Data Model
- The Open Info API para Puertos project Data Nodel covers information of several different domains and, in this project, we had to choose between two possibilities, to define our own dataset or to recommend the use of several datasets that are used by those specific domains.
- As one of our main objectives is to standardize the development of APIs, reusing what others have done before, we have chosen the second alternative and our dataset will be created from others that are used in their specific domain.
- But each organization or association has defined their own dataset metadata and we have to decide how the entities, attributes and metadata are expressed in our proposal and how we recommend to harmonize their semantics.
  