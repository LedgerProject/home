# The  Project

Fairbnb.coop is a platform of tourist services created with the ambition to generate, in travel destinations around the world, communities of reference identity which are bound to the principles of sustainability. Platform tourism, thanks to the cooperative management of Fairbnb.coop, becomes a tool for economic change and the promotion of innovative policies also by local administrations in an open and constant dialogue/debate between all participants in the community.

With this module we are adding a new feature that let Fairbnb.coop be able to certificate listing before they are published. The Fairbnb.coop certificate would mainly prove for a given time the compliance with local regulation, additional policies described by Local Node, and then would contain the info about % of money distribution to the different stakeholders. Certificating for us means both making every host to signs a contract with us to ensure to be compliant with the defined criteria, and then providing a certificate to be shown by the host to any third party that may ask for it.

## The Technology

Currently our booking engine is based on a proprietary platform, because we are evaluating the possibility to rewite everything to be open source, we are evaluating some options, one of which is prestashop. Prestashop is an open source e-commerce platform.
Thus, the module we have developed for our certificate is a prestashop module.

###	Frontend: 

- twig/smarty: twig is the template engine used in the backoffice part while smarty is the template engine used in the frontoffice part (on prestashop)
- jquery: to interact with DOM and backend
- javascript: to interact with local storage
- zenroom: 
  - to generate the hash of the responses required to generate the keypair
  - to generate the keypair
  - to sign the contract
  - to validate the signed contract

###	Backend: 

- php/symfony: used for building a prestashop module and to get the seed necessary for keypair generation (based on hash generated on fronted side)

### Databases:

- mysql: used to store 
  - the responses hash (to validate a keypair reset request)
  - the public key (to verify the certificate)
  - the signed contract for a listing

###	Frontend: 

- twig/smarty
- jquery
- zenroom

## The Repos

https://github.com/LedgerProject/prestashop_attributes_signature_module

This repository contains both backend and frontend code

## The Team


Jonathan Reyes is an urban innovation consultant specialized on the  integration of technology and collaborative culture for the improvement of urban policies. He is cofounder and vicepresident of Fairbnbcoop.

Domenico Di Siena is a civic designer, consultant and researcher who designs and develop process and tools to help communities and organizations collaborate and learn for social good.

Marco Lami is the CTO of Fairbnb.coop, he is a software engineer with more thant 15 year of experiences in building software. For Fairbnb certificate he take care of designing the IT structure and coordinating the software development.

Oleksandr Topov is a young full stack developer with experience in e-commerce platform. For Fairbnb certificate he take care of developing the certification module.

## Use Case Demo

You can try our solution following these steps:

 ### Keypair/certificate generation
 
 ### Certificate validation

