# Semantics

## Semantics is key for the API standardization
- Semantics, in the context of electronic data exchange, is the unambiguous meaning of
each of the pieces of information to be shared between sender, receiver and any stakeholder
who views or uses the information.
## Vocabularies
- A vocabulary define the concepts and relationships ("terms") used to describe and represent a specific domain.
- Vocabularies are used to classify the terms that can be used in a particular application, characterize possible relationships, and define possible constraints on using those terms.
- Their role is to help data integration when ambiguities may exist on the terms used.
- Vocabularies can also be used to organize knowledge. 
- JSON-LD is suitable for publishing vocabularies because it is useful for both humans and machines.
- There are multiple vocabularies, some of them well established, such as schema.org and, for trade, transport and administration there is also the UN/CEFACT vocabulary.
- Schema.org provides the most widely used JSON-LD vocabulary in use today and so is a good guide for what other vocabularies should look like.
- A vocabulary can be published as a file with the reference data models and several files with code lists.
## Reference data model / Common Data Models
- A Reference Data Model (RDM) is an abstract model that organizes Business Information Entities (BIEs) and standardizes how they relate to one another and to the real world. The model provides a standard means by which data may be described, categorized and also shared.
- Data Model contains relationships between tables that which addresses cardinality and nullability of the relationships. 
- A Reference Data Model (RDM) is composed by a set of terms or primary entities / classes / terms and several attributes. 
- Attributes 
- The minimal set of attributes is defined by each initiative and there are several of them, e.g.:
  1. The Dublin Core Metadata Initiative (DCMI).
      - The DCMI define their "terms" with a minimal set of attributes like a:
        - Name
        - Label
        - URI (Uniform Resource Identifier)
        - Definition
        - Type of term
      - And in DCMI, additional information of the primary entities can be provided with other attributes like:
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
      - CEFACT (edi3.org) defines its entities with a minimal set of attributes like a:
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
## Naming and Design Rules (NDR)
- For the deployment of this IDEA, we propose to use existing vocabularies, when it is possible, and according to this decission we can use different vocabularies in our APIs, depending of their Domain. 
- But, not all the Domains covered by our IDEA have a well established vocabulary and we will have to propose our own and therefore we have to establish a Naming and Design Rules.
- Most of the API guidelines include NDR as part of their specification.    
## Code lists
- Some vocabularies are called “codelists”.
- The recommended format for publishing codelists is to use rdf (resource description framework) and a JSON-LD data model.

## Data set
## Data dictionaries
## Linked data
- To make a huge amount of data on the Web available in a standard format, relationships among data should be made available and this collection of interrelated datasets on the Web can also be referred to as Linked Data.
- Integrating facts from several datasets, the application may provide a much better user experience.

 
 
