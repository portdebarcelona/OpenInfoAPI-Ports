# Semantics

## Semantics is key for the API standardization
- Semantics, in the context of electronic data exchange, is the unambiguous meaning of
each of the pieces of information to be shared between sender, receiver and any stakeholder
who views or uses the information (CEFACT, document ECE/TRADE/C/CEFACT/2019/27).
## Some semantic concepts:
### Vocabularies
- A vocabulary defines the concepts and relationships used to describe and represent a specific domain.
- Vocabularies are used to classify the terms (entities) that can be used in a particular application, characterize possible relationships, and define possible constraints on using those terms.
- Their role is to help data integration when ambiguities may exist on the terms used.
- Vocabularies can also be used to organize knowledge. 
- W3C offers a large palette of techniques to describe and define different forms of vocabularies in a standard format. These include RDF and RDF Schemas, Simple Knowledge Organization System (SKOS), Web Ontology Language (OWL), and the Rule Interchange Format (RIF). 
- JSON-LD is also suitable for publishing vocabularies because it is useful for both humans and machines.
- There are multiple vocabularies, some of them well established, such as schema.org and the UN/CEFACT vocabulary is valid for trade, transport, and administration.
- Schema.org provides the most widely used JSON-LD vocabulary in use today and so is a good guide for what other vocabularies should look like.
- A vocabulary can be published as a file with the reference data models and several files with code lists.
### Code lists
- Some vocabularies are called “code lists”.
- The recommended format for publishing code lists is to use rdf (resource description framework) and a JSON-LD data model.
### Data model / Reference data model / Common Data Models
- A Data Model is an abstract model that organizes information entities and standardizes how they relate to one another and to the real world. The model provides a standard means by which data may be described, categorized, and also shared.
- Data Model contains relationships between tables that which addresses cardinality and nullability of the relationships. 
- The main constructs of a Data Model are Entities (terms or instances) and Attributes.
  - Attributes can represent Properties and Relationships. 
  - Entities can be the subject of attributes (properties and relationships). 
  - Properties and relationships can be the subject of other properties and relationships.  
  - **Entities**:
    - Entities represent a thing. 
    - Entities include a semantic type that describes the type of thing represented by the entity.
    - Some examples of entities are person, company, building, ship, container... 
  - **Attributes**: 
    - Attributes are properties of entities.
    - A property is a combination of an attribute and its value.
    - Attributes describe the current state of the entity they belong to.
    - Some nested properties of properties are called metadata. They describe what is the functionality provided by an attribute to the user or a system that reads the attribute.
    - Metadata is data that describes data.
    - Attributes can also provide information on the interactions between entities. Relationships are new types of attributes intended to link one entity to another entity.
    - In some implementations, a relationship is expressed by means of a special attribute with a special value (relationship’s object), that is a URI which points to another entity.  
    - Each implementation defines its minimal set of attributes.
    - Some examples of attributes are for specify:
      - properties, like address, type of ship, temperature, ... 
      - metadata, like date created, accuracy, ...
      - relationships, like a container ship carries several containers and several packages are stuffed on a container.  

- There are several data models and each one establishes the minimum information for defining their entities and attributes, for example:
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


### Datasets
- Datasets are collections of structured metadata
- There are sets of statements about things, where each statement consists of an element ("attribute") of the entity and a "value" for that element.
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
- To make a huge amount of data on the Web available in a standard format, relationships among data should be made available, and this collection of interrelated datasets on the Web is referred to as Linked Data.
- Integrating facts from several datasets, the application may provide a much better user experience.
- JSON-LD offers the capability of expanding JSON terms to URI, facilitating the unambigous definition of terms using vocabularies.
### Context 
- Some API implementations include a hash map used to map member names to URIs (uniform resourde identifiers).
- Those URI can reference a local server, a GitHub URI or a particular URI of an implementation. Each alternative has pros and cons if we think about availability, lenght of the URI or control.  
- This is one example that includes the @context:
```json
      {
        "@context": [
          "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld",
          "https://fiware.github.io/data-models/context.jsonld"
        ]
      } 
``` 
### Naming and Design Rules (NDR)
- Most of the API guidelines include NDR as part of their specification.
- The NDR provides a means to identify, capture and maximize the re-use of business
information components extensions in order to support information
interoperability across integrated environments.
 