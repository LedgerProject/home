# The Gene Coop Project

We provide a consent service for researchers that need to perform research using citizens DNA.

The consent service allows DNA owner to retain control on how their DNA is used in the research for which it is needed.

This service will be part of a citizen-based cooperative that collects DNA for genomic data research, and provides informed consent to its members and fine-grained controlled access for researchers.

## The Technology
 - Back-end: Django/Python (served behind Nginx in production)
 - Front-end: HTML/CSS and Javascript
 - Cryptography: Zenroom used both in the front-end (with javascript binding and browserify) and in the back-end (python bindings)
 
## The Repos

### GeneCoop

- [GeneCoop](https://github.com/LedgerProject/GeneCoop)
The GeneCoop repo contains the Demonstrator Django web application. 
This MVP focuses on two users, the researcher and the 'dna owner'. 
The purpose of this demonstrator is to form a basis to engage stakeholders in discussion and testing. 
Based on the insight gained by this and what we have learned by applying the technology, we will choose and implement what part of the demonstrator to improve.
For example the storage is now on a simple database, but we are thinking about ledger-based approaches.

## Links
The demonstrator interfaces are located [here](https://genecoop.waag.org/request) for the researcher and [here](https://genecoop.waag.org/consent) for the DNA user.
Instructions on how to install the demonstrators are [here](https://github.com/LedgerProject/GeneCoop/tree/master/Demonstrator)
