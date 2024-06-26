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
Although BIDS is intended to be applicable to any business scenario and any business process, including B2B, B2G, G2B, B2C etc. interactions, in this document the focus is on the specific business process of a financial institution doing a KYC (Know Your Customer) check to assess whether it, according to the laws in the jurisdiction it resides in and its internal statutes/xxx, can open a bank account for a business entity that has applied for it.

### 1.1 Know Your Customer -process in the banking sector

When a new business entity starts conducting its business activities, one of the first key capabilities to be implemented is the ability to make and receive payments through the international banking system. For this purpose, the business entity needs to approach a financial institution, like a bank, and apply for the opening of a bank account. Traditionally this has been done locally, probably in one of the branches of a national bank. 

National and international regulation in the business area, especially EU Anti Money Laundering regulation, requires the bank to fulfill a rigorous check of the applicant and its relationships to other entities. 

(Picture: the national legal requirements in Germany as a step-by-step process description)  

![image](https://github.com/EU-Business-Information-Data-Space/BIDS-Rulebook/assets/16665070/ec53a653-a613-4cf1-90cc-b83b2f432800)

Through the introduction of digital means to perform business process functions, many business processes that used to be bound to physical locations and whose execution was carried out by manual activities can nowadays be executed online and be partially or completely automated. One lacking capability in the digital and automated execution of the Know Your Customer process has been the absence of means to prove the identity of a business entity or its representative as well as presenting a trustworthy digital version of the documents that contain the information required in the business process.

With the introduction of the BIDS and the digital capabilities it prescribes, these shortcomings can now be remedied, especially in the siuations where the KYC process is to be executed between a business entity and a financial institution that do not reside in the same jurisdiction.

## 2. Data Providers
In comparison with traditional data sharing initiatives, the Data Providers in the BIDS are always the data subjects themselves, sharing all data according to MyData principles. The data to be shared can either be produced or stored by a third pary, like a government agency that stores information about a business entity in specific registries, or produced by the business entity itself in the form of specific business documents like orders, invoices or receipts.

Source: https://www.w3.org/TR/vc-data-model-2.0/
In the W3C VC world, the Data Product to be shared by the Data Provider is either a VC presentation by the Holder of data issued by an Issuer to the Holder OR the issuance of data by the Holder itself (in the Issuer role)

Example: Company A hands over a trade register extract and an invoice to Company B. The extract is a VC issued by the national registration authority, that A merely "presents" it to B (who acts in the role of a Verifier (or EU: Relying Party), whereas the invoice is created (issued) by A and given to B (who acts in the role of Holder and Relying Party)

![image](https://github.com/EU-Business-Information-Data-Space/BIDS-Rulebook/assets/16665070/add182f0-830e-48e0-b0a3-ce9ab10f74c8)

The approved way of sharing data is in the form of a W3C Verifiable Credential Presentation, which means that Data Providers, aka the business entities themselves, need to be equipped with the capability of making presentations of verifiable credentials.

In order for the BIDS to work properly also the actors who act as an authentic source for a certain data product, mainly governmental agencies who have the legal right to maintain registries of a certain type, need to have the capability to issue data products in the form of verifiable credentials to the digital wallets of the business entities.

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

In the BIDS context, all data to be shared MUST be described as application profiles in the SHACL Shape technical format. See visualization [here](semantic-technical-modeling.md)

NOTE: The proposed common toolset for BIDS specific semantic modeling according to the described methodology is the Interoperability Platform, consisting of the Terminologies tool (https://sanastot.suomi.fi/), Data Vocabularies tool (https://tietomallit.suomi.fi/ and Reference Data tool (https://koodistot.suomi.fi/). However, since the platform is currently maintained only for use by the Finnish public anc private sector organizations, a new governance model for the tools needs development in the BIDS context.

NOTE: In the DSSC Blueprint v1.0 context, the contents of this chapter are described in a generic visualization:
![image](https://github.com/EU-Business-Information-Data-Space/BIDS-Rulebook/assets/16665070/c23f25cd-c818-4a58-ade3-bd0e92a4d2c6)


### 4.1 Organization and governance of the required common data modeling
A Semantic Working Group is to be established for the creation of the common ontology, vocabularies, code lists and application profiles that the Governance Body decides to be necessary for the data sharing in different business process contexts.

The participants of the Semantic Working Group SHALL at least represent each national business registration authority, but additional members are to be included depending on the scope of business processes that are covered by the BIDS. In the KYC case, the SWG should appoint members also from national tax authorities as well as from organizations representing actors in the banking sector and financial institutions.  

## 5. Allowed technical data sharing mechanisms
The data that is shared by the Data Providers and consumed by Data Consumers in the BIDS context SHALL be available as W3C Verifiable Credentials, specifically in the format and through the protocols etc. that are to be defined in the context of the eIDAS 2.0 regulation.

The probably most suitable technical format for the verifiable credentials (or (Q)EAAs in an EU context) is going to be the SD-JWT VCDM, which allows for the credential subject to be described in JSON-LD (is this correct?)

https://github.com/danielfett/sd-jwt-vc-dm
 
### 5.1. Organization and governance of the technical data sharing

### 5.2. Schema repository with approved credential schemas
In the context of eIDAS 2.0 compliant digital wallets, the ARF (in its 1.4.0 version) states the following about "catalogues":
![image](https://github.com/EU-Business-Information-Data-Space/BIDS-Rulebook/assets/16665070/0aa5f5dc-eb98-4d8c-a83c-7686f5fce2a5)

In the context of BIDS, such a catalogue will be solely based on the JSON-LD schemas derived automatically from the SHACL Shapes (application profiles) that describe the semantics of each data product (which in the context of eIDAS 2.0 are called (Qualified) Electronic Attestations of Attributes. The best way of making these mandatory semantic data descriptions and their technical implementations available needs further investigation.  

In the meantime, a list of links to all relevant Data Product descriptions (consisting a "schema registry") can be found [here](credential-schemas.md)

## 6. Model for the overall organization and governance of the BIDS
According to the DSSC Blueprint v1.0 (https://dssc.eu/space/BVE/357074549/Organisational+Form+and+Governance+Authority) the most suitable model of governance for the BIDS could be an EDIC.
