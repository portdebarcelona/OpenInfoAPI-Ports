# Semantics

**Semantics** is a key piece in the exchange of information between applications and, therefore, it is also key in the standardization of APIs.

According to UN/CEFACT, in the context of electronic data exchange, is the unambiguous meaning of each of the pieces of information to be shared between sender, receiver and any stakeholder who views or uses the information (CEFACT, document ECE/TRADE/C/CEFACT/2019/27).

In order to develop this section, it is considered necessary to define several concepts related to semantics in the exchange of information between applications. Among them the concepts of domain, vocabulary, code lists, data model, entity, attribute and metadata.

### Domain
- Discipline or specific field of knowledge, as opposed to general knowledge.

### Vocabulary
- It defines the concepts and relationships that are used to describe and represent a specific domain.
- Vocabularies are used to classify the entities that can be used in a particular application, characterize possible relationships, and define possible restrictions on the use of those entities or terms.
- Its function is to help data integration when there may be ambiguities in the terms used.
- Some examples of vocabularies are that of schema.org or that of UN/CEFACT

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
### Entities (terms or instancies)
  - Entities represent a thing. 
  - Entities include a semantic type that describes the type of thing represented by the entity.
  - Some examples of entities are person, company, building, ship, container...

### Attributes
  - Attributes can represent properties and relationships of entities.
  - A property is a combination of an attribute and its value. 
  - Attributes describe the current state of the entity they belong to. 
  - Some examples of attributes are used to specify properties, such as direction, ship type, temperature, ... or to specify relationships, such as a container ship carrying multiple containers containing multiple packages.

### Metadata
Some properties are called metadata. They describe what functionality is provided by an attribute to the user or a system that reads the attribute. Metadata is data that describes data. Some examples of metadata are the date of creation, the precision of a data, ...


# Top-down approach
- A top-down approach will be followed to define the data model for "Open Info API para puertos", following these steps:
  1. Identification of the **domains** that will be covered in the project.
  2. Identification of several operations for the **APIs** for each domain.
  3. Definition of **input and output parameters** of those APIs.
  4. From parameters to **entities and their attributes**.


## Domains
- Although it is a list that can always be expanded, the following domains appear in this initial version:
  1. **Ships Calls**. Information about actual or planned ships calls at a specific port. Including scheduled arrivals and departures.
  2. **Liner Services**. Information of liner services, carriers involved and ports serviced. 
  3. **Port Infrastructure**. Basic data of the infrastructure of a port, its land and sea accesses, its terminals and its railway infrastructure. 
  4. **Port Procedures**. Links to the websites where all port procedures of a port are described.
  5. **Statistics**. Traffic and economic statistics of a port.
  6. **Environment** This domain covers weather, sea state and pollution information associated to a port.
  7. **Rail Transport** Information about rail transport in ports, including their rail connections, linked railway terminals, train arrivals and departures and information about all the actors involved in this type of transport.
  8. **Vehicle Traffic Monitoring** Information about the number of vehicles entering or leaving a port area.
  9. **Terminals** Information about terminal performance, including the number of cargo units that enter or leave from a terminal per hour, the number of cargo units loaded or unloaded per hour from vessels or the wait time of trucks to enter to a terminal.
  10. **News** News from a port, including the possibility to subscribe to a service of news. 
  11. **Notices** Notices of interest from a port, including the possibility to subscribe to a service of port notices. 
  12. **Port Rates and Fees** Link to the web page where port rates and fees of a port are published. 
  13. **Port Services** Information about services that are offered by a port and which vessels can order those services. E.g.: bunkering, marpol, mooring, pilots, tugs,...
  14. **Port Calendar** Information about working days, weekend days, and list of public holidays from the requested date period and port.
  15. **Port Directory** Information about companies and administrations that operate in a port.

## Catalog of APIs
- Although initially it was thought to develop an API with its specific operations for each of the identified domains, it was finally decided to develop a single API and identify the domains by means of “tags”. 
- In the API described, 76 operations have been proposed, 68 GET requests and 8 POST requests.
- E.g. in the road traffic domain, a GET operation has been provided to obtain the waiting time to enter a terminal or, in the notices domain, a POST operation has been provided to request subscription to a specific port notices service. 
- [Here](./CatalogIntroduction.md) there are some initial examples of possible APIs.

## APIs' Input and Output Parameters
- For each of the proposed API operations, whether of the GET or POST type, their input and output parameters were defined.
- Using the same examples of the previous point, in the first case, in the GET operation of the domain on road traffic, the code of the port and the terminal were defined as input parameters and, as a response, it was determined that the code of the terminal and the access time expressed in minutes, in addition to reporting on the values indicated when formulating the query and including a series of metadata that will be provided in all the responses to the operations of the Open Info API initiative for ports.
- These common metadata comprise a unique request identification code (requestId), the date the response data was created (dateCreated), the last date it was modified (dateModified) and the date the response was retrieved. information (dateRetrieved):

        
        metadata:
          description: Metadata information associated to a response.
          type: object
          properties:
            requestId:
              description: Unique identifier of the request. Include this as reference when reporting issues.    
              type: string         
            dateCreated:    
              description: Entity creation timestamp. This will usually be allocated by the storage platform.    
              type: string 
              format: date-time      
            dateModified:    
              description: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.    
              type: string   
              format: date-time    
            dateRetrieved:    
              description: The date and time the information was retrieved in ISO8601 UTC format.      
              type: string    
              format: date-time  

- In the second example, in which a POST operation is defined to request subscription to a certain notification service of a port, the entry of a series of subscriber data has been foreseen, such as their contact information (telephone or email ), name, surname, company, categories of notices to which you want to subscribe and language in which you want to receive the notices, being necessary to include at least the contact information, the categories of notices and the language.

- And, in response, a reference to the subscription request is expected to be received, which, in turn, will contain a reference to that subscription request and a message associated with that subscription.

      subscriptionReference:
        description: Response after a subscription request has been received
        type: object
        properties:
          subscriptionRequestReference:
            $ref: '#/subscriptionRequestReference'
          subscriptionRequestMessage:
            $ref: '#/subscriptionRequestMessage'

      subscriptionRequestReference: 
        description: Reference assigned to a subscription request.
        type: string
        example: '2022-02-07T17:05:12_REF001'

      subscriptionRequestMessage:
        description: Response message to a subscription request. 
        type: string 
        example: 'Your subscription request has been received and soon you will receive a validation code (email/sms)'


- Within the [catalog of APIs](./CatalogIntroduction.md), accompaining each example of API, there is also a list with its input and output parameters.

## Entities and attributes
- There are initiatives that propose their own data models and each one establishes the minimum information to define their entities and attributes. Some of the best known are the Dublin Core Matadata Initiative (DCMI), which defines its "terms" (entities) with a minimum set of attributes such as name, label, URI (Uniform Resource Identifier), definition and term type. It also envisions that additional information from primary entities may be provided with other attributes. Another initiative is CEFACT, which defines its entities with a minimum set of attributes such as its identification, type, comment, label and a series of metadata, each of them including its identification, type, cefactUNId, comment and cefactBus.

- For the Open Info API for Ports initiative, it is proposed to always include the following attributes already provided in OpenAPI:
  -	Name
  -	Description
  -	Type
- And include on certain occasions other attributes such as:
  -	Example
  -	Minimum length
  -	Maximum length
  - List of possible values

 