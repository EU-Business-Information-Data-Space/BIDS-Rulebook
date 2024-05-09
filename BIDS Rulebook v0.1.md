# Business Information Data Space Rulebook
### Version 0.1

#### Contents

1. Description of Business Scenario where data is to be shared
2. Data Providers
3. Data Consumers
4. Methodology for defining the data to be shared
5. Allowed technical data sharing mechanisms
6. Model for the overall organization and governance of the BIDS

## 1. Description of Business Scenario(s) where data is to be shared

When a new business entity starts conducting its business activities, one of the first key capabilities to be implemented is the ability to make and receive payments through the international banking system. For this purpose, the business entity needs to approach a financial institution, like a bank, and apply for the opening of a bank account. Traditionally this has been done locally, probably in one of the branches of a national bank. 

Through the introduction of digital means to perform business process functions, many business processes that used to be bound to physical locations and whose execution was carried out by manual activities can nowadays be executed online and be partially or completely automated. One lacking capability in the digital and automated execution of the Know Your Customer process has been the absence of means to prove the identity of a business entity or its representative as well as presenting a trustworthy digital version of the documents that contain the information required in the business process.

With the introduction of the BIDS and the digital capabilities it prescribes, these shortcomings can now be remedied, especially in the siuations where the KYC process is to be executed between a business entity and a financial institution that do not reside in the same jurisdiction.

## 2. Data Providers
In comparison with traditional data sharing initiatives, the Data Providers in the BIDS are always the data subjects themselves, sharing all data according to MyData principles. The data to be shared can either be produced or stored by a third pary, like a government agency that stores information about a business entity in specific registries, or produced by the business entity itself in the form of specific business documents like orders, invoices or receipts.

The approved way of sharing data is in the form of a W3C Verifiable Credential Presentation, which means that Data Providers, aka the business entities themselves, need to be equipped with the capability of making presentations of verifiable credentials.

The technical format for this data sharing capability is described in Chapter 5.

## 3. Data Consumers
The approved way of consuming data that is shared by the Data Providers is through the reception of Verifiable Credential Presentations in the role of a Verifier or Relying Party, following closely the specifications of the W3C Verifiable Credentials specification as well as the eIDAS 2.0 regulation and it's Implementing Acts.

The technical format for this data consuming capability is described in Chapter 5.

## 4. Methodology for defining the data to be shared
The data to be shared is to be defined and described according to the following

- A SKOS ontology MUST be developed, covering all necessary concepts that are needed to describe the data to be shared in the specific business process context. Only English SHALL be the compulsory language used in the creation of the ontology, but other EU languages can be used in parallell.
- A RDF/OWL Vocabulary SHALL be developed based on the beforementioned SKOS ontology, linking classes, attributes and associations to the concepts in the ontology.
- The Classes, Attributes and Associations in the Vocabulary SHALL be linked to the global, regional or domain-specific vocabularies that the Governing Body decides to be relevant for the BIDS. Linking SHALL take place as either rdf:superClass or rdf:equivalentClass references.
- Application profiles in the form of SHACL Shapes SHALL be developed by specializing the common domain-specific RDF/OWL Vocabulary classes, attributes and associations in the RDF/OWL Vocabulary.
- Attribute enumeration values CAN be specified as code lists if necessary

In the BIDS context, all data to be shared MUST be described as application profiles in the SHACL Shape technical format.

NOTE: The proposed common toolset for BIDS specific semantic modeling according to the described methodology is the Interoperability Platform, consisting of the Terminologies tool (https://sanastot.suomi.fi/), Data Vocabularies tool (https://tietomallit.suomi.fi/ and Reference Data tool (https://koodistot.suomi.fi/). However, since the platform is currently maintained only for use by the Finnish public anc private sector organizations, a new governance model for the tools needs development in the BIDS context.

### 4.1 Organization and governance of the required common data modeling
A Semantic Working Group is to be established for the creation of the common ontology, vocabularies, code lists and application profiles that the Governance Body decides to be necessary for the data sharing in different business process contexts.

The participants of the Semantic Working Group SHALL at least represent each national business registration authority, but additional members are to be included depending on the scope of business processes that are covered by the BIDS. In the KYC case, the SWG should appoint members also from national tax authorities as well as from organizations representing actors in the banking sector and financial institutions.  

## 5. Allowed technical data sharing mechanisms
The data that is shared by the Data Providers and consumed by Data Consumers in the BIDS context SHALL be available as W3C Verifiable Credentials, specifically in the format and through the protocols etc. that are to be defined in the context of the eIDAS 2.0 regulation.

## 6. Model for the overall organization and governance of the BIDS
According to the DSSC Blueprint v1.0 (https://dssc.eu/space/BVE/357074549/Organisational+Form+and+Governance+Authority) the most suitable model of governance for the BIDS could be an EDIC.

### 5.1. Organization and governance of the technical data sharing


### 5.2. Schema repository with approved credential schemas
See see documentation [here](credential-schemas.md)
