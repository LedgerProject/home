<!-- PROJECT LOGO -->
<br />
<p>
  <h3>The Smart Consent Project</h3>
  <img src="https://github.com/LedgerProject/eprocessmed-smc-app/raw/master/smart-consent/src/assets/img/logo.png" />
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
* [BlockChain Description](#blockchain-description)


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

## The Technology

Using Express with NodeJS, ApiREST has been built that give access to the data to the FrontEnd that is built in AngularJS. Similarly, using NodeJS together with Web3.js, access points have been built to communicate the FrontEnd with the Alastria blockchain.

## Software used

* [npm](https://www.npmjs.com)
* [Visual Studio Code](https://code.visualstudio.com)
* [Postman](https://www.postman.com)
* [GitHub](https://github.com)


##  Directory structure 

 - In "smart-consent" is the new frontend structure.
 - In "api_df_middleware" is a business middle layer.
 - In "api_df_back" contains the data models.
 - In "apiblockchain" It contains an api that gives access 
   to the frontend to interact with the Alastria blockchain.


## Starting a development environment

### Prerequisites

* npm and node.js: first of all install npm and node.js (https://nodejs.org/it/download/)

* Angular CLI: install the Angular CLI (https://angular.io/guide/setup-local)


npm install


## Available scripts

To run each project:

To run api_df_middleware:
```sh
/api_df_middleware/src$ node app.js
```

To run api_df_back:
```sh
 /api_df_back/src$ node app.js
```

To run the rest api to access the blockchain:

```sh
npm run test
```

To run smart-consent FRONT:
```sh
ng serve
```

## Links

Application link: [E-processmed](https://e-processmed.com/)


# BlockChain Description
  API REST NodeJS: 
  access to the Alastria blockchain
