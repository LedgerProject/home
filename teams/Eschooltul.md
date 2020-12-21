# The Eschooltul Project

[Eschooltul]((https://eschooltul.com)) is a tool that serves families, institutions and schools by providing sovereign control over children's sensitive data.
We secure the Students’ Digital Files by recording the accesses to it, and storing hashes of its contents in a Blockchain in order to guarantee the integrity of the data. In the future, Eschooltul also intends to store the original data on the Blockchain, to facilitate interoperability.

## The Technology 

Eschooltul offers an open source and free network, in which tutors, institutions and developers will have full free access to the code. They may also contract us to carry out integrations with their ERP’s or other software. Using Eschooltul, with a very intuitive web app interface, they may upload data to the blockchain, and/or consult it to verify the information hashes and accesses.
Given the criticality of the data handled, the main technological requirement is that each part of this project complies with the application of the seven foundational principles of privacy by design. 

For that reason, we are analyzing several distributed ledger technologies to choose the one that best suits the needs of the project. 

- We are using Ruby and [Ruby on Rails Framework](https://rubyonrails.org/) (v6.1) for the application. 
- For the Database we are using [PostgreSQL](https://www.postgresql.org/) (v11).
- For the server we are using a Digital Ocean droplet with [Dokku](https://github.com/dokku/dokku). We have SSL through letsencrypt. 
- The application is accessible through [https://eschooltul.com](https://eschooltul.com).

###  Repo-Backend
 - [Eschooltul_Backend](https://github.com/LedgerProject/eschooltul_backend)
 - ***Eschooltul_Backend*** does basic cryptography and contains most of the business logic
 - It requires Ruby on Rails 6
 - It connects to PostgreSQL > 11
 
