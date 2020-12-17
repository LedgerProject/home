# The LiV Project

Inheritance is currently a complex, bureaucratic and paper-based process. LiV sees an opportunity to improve the way in which these interactions and services take place. LiV is a web platform built on blockchain and other technologies that addresses authentication & confidentiality issues and protecting users. LiV aims to simplify processes, reduce risks, time and costs for the ecosystem.


## The Technology

LiV will be using decentralised technologies with an encryption component. We plan on leveraging existing developments done by other LEDGER participants (we are in particular considering Unified Science).  LiV aims to create a simple and interactive Graphical User Interface for communicating with the blockchain system.
We are evaluating the use of a public non-permissioned blockchain, with smart contracts with restricted users that can interact with, as a permissioned contract.
Further assessment of existing LEDGER components and developments needs to be done to ensure synergies and collaboration are maximised. 

As it is known, the blockchain ledger is immutable and information that is stored in it can not be removed, modified, backdated or manipulated in any other way. This poses a challenge for the project to be GDPR-compliant since one of the ground points of the regulation is that the personal information about the user should be removed by their request. Thus, to make a solution compliant with the principles of GDPR we have designed a system in such a way that the blockchain ledger does not store any information that, when retrieved, can identify the user.

However, an important goal of the project was to provide verifiability and traceability of actions that are happening by leveraging the features of blockchain-based systems described at the beginning. To tackle both of these requirements we have designed the system in  such a way, that blockchain stores only hashes of events and digital signature values that can be verified by any party even if it doesn't know who generated the signature and digital identifiers that are not directly tied to the identification information of the party who generated the signature.

The hash function is a one-way transformation that, unlike encryption, does not allow to retrieve the original data from the hash. However, the party that is authorised and received user's consent to their personal data is able to do execute the hashing function on its premise and unequivocally verify that the hash of this dataset is present in the blockchain. If the outside auditor is present in the system, it can also verify the digital signatures making sure that actions happening in the system are legitimate even without having any access to the actual personal data of the user

## The Repos

### LiV_backend
 - [LiV_backend](https://github.com/LedgerProject/LiV_backend)
 - ***LiV_backend*** implements the necessary cryptographic functionality, connectivity modules for permissioned blockchain network and REST API for integration with the frontend application
 - It requires JRE or JDK version 1.8.0_271
 - It communicates with LiV_frontend
 
### LiV_frontend
 - [LiV_frontend](https://github.com/LedgerProject/LiV_frontend)
 - ***LiV_frontend*** 
 - It requires Vue.js version 2.6.11 or higher
 - It communicates with LiV_backend
