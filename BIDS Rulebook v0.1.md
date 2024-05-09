# Business Information Data Space Rulebook
### Version 0.1

#### Contents

1. Description of Business Scenario where data is to be shared
2. Data Providers
3. Data Consumers
4. Methodology for defining the data to be shared
5. Allowed technical data sharing mechanisms

## 1. Description of Business Scenario(s) where data is to be shared

When a new business entity starts conducting its business activities, one of the first key capabilities to be implemented is the ability to make and receive payments through the international banking system. For this purpose, the business entity needs to approach a financial institution, like a bank, and apply for the opening of a bank account. Traditionally this has been done locally, probably in one of the existing bank 

## 2. Data Providers
In comparison with traditional data sharing initiatives, the Data Providers in the BIDS are always the data subjects, sharing either data


## 4. Methodology for defining the data to be shared
The data to be shared is to be defined and described according to the following

- A SKOS ontology MUST be developed, covering all necessary concepts that are needed to describe the data to be shared in the specific business process context. Only English SHALL be the compulsory language used in the creation of the ontology, but other EU languages can be used in parallell.
- A RDF/OWL Vocabulary SHALL be developed based on the beforementioned SKOS ontology, linking classes, attributes and associations to the concepts in the ontology.
- Application profiles in the form of SHACL Shapes SHALL be developed by specializing the common domain-specific RDF/OWL Vocabulary classes, attributes and associations 

In the BIDS context, all data to be shared MUST be described as application profiles in the SHACL Shape technical format.


## 5. Allowed technical data sharing mechanisms
