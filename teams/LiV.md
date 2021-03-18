# The LiV Project

Inheritance is currently a complex, bureaucratic and paper-based process. LiV sees an opportunity to improve the way in which these interactions and services take place. LiV is a web platform built on blockchain and other technologies that addresses authentication & confidentiality issues and protecting users. LiV aims to simplify processes, reduce risks, time and costs for the ecosystem.


## The Technology

LiV will be using decentralised technologies with an encryption component. We plan on leveraging existing developments done by other LEDGER participants (we are in particular considering Unified Science).  LiV aims to create a simple and interactive Graphical User Interface for communicating with the blockchain system.
We are evaluating the use of a public non-permissioned blockchain, with smart contracts with restricted users that can interact with, as a permissioned contract.
Further assessment of existing LEDGER components and developments needs to be done to ensure synergies and collaboration are maximised. 

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
