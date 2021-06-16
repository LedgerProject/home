# The Eschooltul Project

Eschooltul is a tool that serves families, institutions and schools by providing sovereign control over children's sensitive data.

We secure the Students’ Digital Record ([SDRs](https://administracionelectronica.gob.es/cise/1606/activosSemanticos))  by recording the accesses to it, and storing hashes of its contents in a Blockchain in order to guarantee the integrity of the data. 

In the future, Eschooltul also intends to store the original data on the Blockchain (maybe using [IPFS](https://ipfs.io/)), to facilitate interoperability.


## The Technology

Eschooltul offers an open source and free network, in which tutors, institutions and developers will have full free access to the code. They may also contract us to carry out integrations with their ERP’s or other software. Using Eschooltul, with a very intuitive web app interface, they may upload data to the blockchain, and/or consult it to verify the information hashes and accesses.

Given the criticality of the data handled, the main technological requirement is that each part of this project complies with the application of the seven foundational principles of privacy by design.

From a technological point of view, we are going to use the following stack:

- We are using Ruby and [Ruby on Rails Framework](https://rubyonrails.org/) (v6.1) for the application. 
- For the Database we are using [PostgreSQL](https://www.postgresql.org/) (v11).
- For the server we are using a Digital Ocean droplet with [Dokku](https://github.com/dokku/dokku). We have SSL through letsencrypt. 
- Blockchain and SmartContracts: [Hyperledger Sawtooth](https://www.hyperledger.org/use/sawtooth) and [Zenroom](https://zenroom.org/). For the moment we only use [apiroom](https://apiroom.net/) with sawroom connector in order to write and read data into/from the Blockchain.

For the moment, we do not have mobile application, only webapp. 

## The Repos

###  Repo-Backend
 - [Eschooltul-Backend](https://github.com/LedgerProject/eschooltul_backend): MVC Rails application that connects to Zenroom
 - It requires Node-JS 14 or above
 - It requires Ruby on rails 6.X and PostgreSQL >= 11.X

## Links

- Landing page: [https://eschooltul.com](https://eschooltul.com)
- Web Application: [https://portal.eschooltul.com](https://portal.eschooltul.com)

![Ledger Logo](https://ledgerproject.eu/wp-content/uploads/2019/09/logo-l-h.png)


