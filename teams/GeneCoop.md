# The Gene Coop Project

Citizen cooperative that provides fine-grained user controlled access and informed consent to genomic data for research.

## The Technology
 - Django
 - Zenroom/Hyperledger
 - LabSpace platform at SURF. It consists of the SURF research cloud and federated identity access management system. On top of this cloud infrastructure we have a DNA test and QA/QC service where we can link identifiers for data curation. These identifiers are a key part of the total system architecture and need to be linked to the consent services we develop.

## The Repos

### GeneCoop

- [GeneCoop](https://github.com/LedgerProject/GeneCoop)
The GeneCoop repo for now contains the Demonstrator Django web application. 
It is a proof of concept that focuses on two users, the researcher and the 'dna owner'. 
The purpose of this demonstrator is to help us figure out the essential technical challenges of the project. 
In a later stage of development parts of this demonstrator can be replaced by other technology, for example something based on the decode app.

## Links
The demonstrator interfaces are located [here](http://135.181.106.35/request) and [here](http://135.181.106.35/consent)
