# The  Project

Fairbnb.coop is a platform of tourist services created with the ambition to generate, in travel destinations around the world, communities of reference identity which are bound to the principles of sustainability. Platform tourism, thanks to the cooperative management of Fairbnb.coop, becomes a tool for economic change and the promotion of innovative policies also by local administrations in an open and constant dialogue/debate between all participants in the community.

With this module we are adding a new feature that let Fairbnb.coop be able to certificate listing before they are published. The Fairbnb.coop certificate would mainly prove for a given time the compliance with local regulation, additional policies described by Local Node, and then would contain the info about % of money distribution to the different stakeholders. Certificating for us means both making every host to signs a contract with us to ensure to be compliant with the defined criteria, and then providing a certificate to be shown by the host to any third party that may ask for it.

## The Technology

Currently our booking engine is based on a proprietary platform, because we are evaluating the possibility to rewite everything to be open source, we are evaluating some options, one of which is prestashop. Prestashop is an open source e-commerce platform.

### First MVP
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

https://github.com/LedgerProject/FairBnb_attributes_signature_module

This repository contains both backend and frontend code

### Final MVP
The final MVP is a complete rewrite of the First MVP. At that time we were evaluating several options to start building our new Open Source platform and Prestashop CMS was one of that. For this reason we build the first MVP as a Prestashop module. The final MVP is a php/Laravel module because php/Laravel is the stack we decided to use for our new platform.

###	Frontend: 

- blade: blade is the template engine used in Laravel
- jquery: to interact with DOM and backend
- javascript: to interact with local storage
- zenroom: 
  - to generate the hash of the responses required to generate the keypair
  - to generate the keypair
  - to sign the contract
  - to validate the signed contract
  - to store the certificate in sawtooth blockchain

###	Backend: 

- php/laravel

### Databases:

- mysql: used to store 
  - the responses hash (to validate a keypair reset request)
  - the public key (to verify the certificate)
  - the signed contract for a listing
  - the hash/id of sawtooth blockchain
## The Repos

https://github.com/LedgerProject/fairbnb-faircert

This repository contains both backend and frontend code

## The Team


Jonathan Reyes is an urban innovation consultant specialized on the  integration of technology and collaborative culture for the improvement of urban policies. He is cofounder and vicepresident of Fairbnbcoop.

Domenico Di Siena is a civic designer, consultant and researcher who designs and develop process and tools to help communities and organizations collaborate and learn for social good.

Marco Lami is the CTO of Fairbnb.coop, he is a software engineer with more thant 15 year of experiences in building software. For Fairbnb certificate he take care of designing the IT structure and coordinating the software development.

Oleksandr Topov is a young full stack developer with experience in e-commerce platform. For Fairbnb certificate he take care of developing the certification module.

## Use Case Demo (First MVP)

You can try our solution following these steps:

 ### Keypair/certificate generation
 
 1) Go to demo website backoffice (https://ledger.fairbnb.coop/admin169jfftgg) user: demo@demo.com password: demodemo
 2) Navigate on the left menu to Parametri Avanzati > Local Ambassador Key Gen
 3) Click on  'Generte key' to obtain the private/public keys filling at leat 3 answers and your email address

 NOTE: 
 now there is no way to create a new keipair if it has been already generated. You can regenerate it aswering to the same questions you've filled in the first time,
 with the same values. For this reason, if you want to genereate a key to test the signature, you need to fill the first 3 questions with 'demo' and use 'demo@demo.com'
 
 4) Once your public/private keys are generated (private key is store into the browser local storage) you can sign a contract selecting it from the dropdown and clicking on 'Sign Contract'
 5) You will see the signed contract inside the textarea on the right
 
 
 ### Certificate validation
 
 1) Go to demo website (https://ledger.fairbnb.coop)
 2) Open listing details
 3) On the right side of the listing detail, you will find the certificate details
 4) If the certificate exists, you will find:
  - the signed contract
  - the public key (you can use to validate/verify the signed contract)
  - the signature
 5) You can also validate the contract from this detail page clicking on 'Verify Sign'

## Use Case Demo (Final MVP)
1) Go to demo website backoffice (https://staging-ledger.fairbnb.coop/) user: demo@demo.com password: Demo@123
2) Rules management: click on hamburgher menu and select 'Rules'
3) Badges management: click on hamburgher menu and select 'Badges'
4) Certify listing: click on hamburgher menu and select 'Listing'
5) Click on 'Waiting for certification' to filter the listings to be certified
6) Click on 'View' to open a detailed view
7) Check all the hard rules to enable the certify button and click on it to certify the listing
8) Click on 'View as Guest' (this button will appear only when the certificate has been created) to have an overview of what a guest can see
9) In this view, you can scroll to the Fairness section to be able to view the certificate, download it, download the public key needed to verify the signature and the sawtooth hash/id 
