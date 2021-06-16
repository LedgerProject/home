# The Gene Coop Project

We provide a consent service for researchers that need to perform research using citizens DNA.

The consent service allows DNA owner to retain control on how their DNA is used in the research for which it is needed.

This service will be part of a citizen-based cooperative that collects DNA for genomic data research, 
and provides informed consent to its members and fine-grained controlled access for researchers.

## The Technology
 - Back-end: Django/Python (served behind Nginx in production)
 - Front-end: HTML/CSS and Javascript
 - Front-end: Web extensions to be installed in the browser (Firefox)
 - Cryptography: Zenroom used both in the front-end (with javascript binding and browserify) and in the back-end (python bindings)
 - Consent format: W3C [Verifiable Credentials](https://www.w3.org/TR/vc-data-model/) to support (semantic) interoperability of our approach.
 
## The Repos

### GeneCoop

GeneCoop [repo](https://github.com/LedgerProject/GeneCoop) contains the Demonstrator Django web application and the web extensions.

This MVP focuses on two users, the researcher and the 'dna owner'. 

We have made considerable use of cryptography to minimize personal data we collect and to build an architecture that can be trusted, 
trust being a fundamental part of our interaction with users.

We also implemented a stardard form of representing our consent with the adoption of W3C VC. 
This has been done in order to minimize the dependency of our consent solution from any technology and create an open environment 
that should encourage third parties to collaborate with us.

## Links
Instructions on how to install the demonstrator and how to operate it are [here](https://github.com/LedgerProject/GeneCoop/tree/master/Demonstrator).

The project website is [here](https://geneconsent.eu).

The online demo is [here](https://genecoop.waag.org). From that page you can access the two user interfaces of the project:
- the researcher [interface](https://genecoop.waag.org/request)
- the DNA donor [interface](https://genecoop.waag.org/consent).

