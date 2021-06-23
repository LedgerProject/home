<!-- PROJECT LOGO -->
<br />
<p>
  <h3>The Smart Consent Project</h3>
  <img src="https://github.com/LedgerProject/eprocessmed-smc-app/raw/master/frontend/src/assets/logo.png" />
</p>

<!-- GETTING STARTED -->
## Table of contents

* [SmartConsent Project](#smartconsent-project)
* [Build with](#built-with)
* [The Technology](#the-technology)
* [Software Used](#software-used)
* [Directory structure](#directory-structure)
* [Starting a development environment](#starting-a-development-environment)
* [Available scripts](#available-scripts)
* [Links](#links)
* [BlockChain Description](#blockChain-description)


## SmartConsent Project

eHealth startup focused exclusively on the digitization of medical processes, has technologically advanced the medical informed consent in security and communication.
It helps the understanding of the patient and offers security using blockchain technology in each step of the informed consent.

* For the patient: Facilitates understanding and acceptance of the indicated procedure; reduces doubts, uncertainties and fears derived from ignorance.

* For the professional: It standardizes the information presented to the patient, fully and absolutely ensures the integrity of the Signed Consent, reduces document costs and process times.

## Built with

* [NodeJS 14](https://nodejs.org/en/)
* [Angular 11](https://angular.io/)
* [Typescript](https://www.typescriptlang.org)
* [Web3js](https://web3js.readthedocs.io/)
* [Flutter](https://flutter.dev/)
* [Python 3](https://www.python.org/)


## The Technology

Web frontend have been built in Angular JS and mobile in Flutter 2.0. The business and access layers to BDD are implemented in NodeJS. APIs are implemented for encryption and file sharing with IPFS. NodeJS is used with Web3.js to communicate the FrontEnd with the Alastria blockchain.

## Software used

* [npm](https://www.npmjs.com)
* [Visual Studio Code](https://code.visualstudio.com)
* [Postman](https://www.postman.com)
* [GitHub](https://github.com)


##  Directory structure 

 - In "frontend" contains the implemented components of the web application 
 - In "mobile" contains the implemented components of the mobile application   
 - In "middleware" contains the business rule APIs
 - In "backend" contains the database access components.
 - In "api_blockchain" It contains an api that gives access 
   to the frontend to interact with the Alastria blockchain.
 - In "api_ipfs" It contains an api that gives access 
   to the frontend to interact with the IPFS blockchain.


## Starting a development environment

### Prerequisites

* npm and node.js: first of all install npm and node.js (https://nodejs.org/it/download/)

* Angular CLI: install the Angular CLI (https://angular.io/guide/setup-local)

* Flutter: install the Flutter 2.0 (https://flutter.dev/)

* Python 3 with Django Rest Framework  (https://www.python.org/)


npm install      
flutter pub get

## Available scripts

To run each project:

To run backend:
```sh
/backend/src$ node app.js
```

To run middleware:
```sh
 /middleware/src$ node app.js
```

To run the rest api to access the blockchain IPFS:

```sh
npm run test
```


To run the rest api to access the blockchain Alastria:

```sh
source env/bin/activate
python manage.py runserver 0.0.0.0:3009
```


To run frontend:
```sh
ng serve
```

To run Mobile:
Additionally you can also execute the f5 key to execute the project
```sh
flutter pub get
flutter packages get
flutter clean
flutter run 
```

To run WhatsApp API:
```sh
npm run test
```

To run Ncrypt/Decrypt API:
```sh
npm run test
```

## Links

Application link: [E-processmed](https://ledger.e-processmed.com/login)


# BlockChain Description
*  API REST in Python access to the Alastria blockchain
*  IPFS REST API in Nodejs
 
