# The Global Passport Project
![Global Passport Project Logo](https://raw.githubusercontent.com/LedgerProject/GPP_backend/main/logo.png)

Global Passport Project is a breakthrough initiative that leverages on decentralized technology to support mixed migrants along their journey, protect their privacy while reporting human rights violations, and engage them as citizens integrating in their new communities. GPP will also enormously improve the capacity of NGOs and social enterprises to reach out to migrants and design their actions, thus streamlining their resources and improving their performance and records when applying for funds and calls.

GPP is a blockchain-based platform with a website and mobile App through which mixed migrants can safely store important documents, access info on
the countries crossed and the solidarity network in the area they are in, as well as report on abuses they might face along the journey. All data is personal and inviolable, and it will be kept on Blockchain with a double-level encryption component.

* GPP’s key tool is the first ever DocWallet, a unique and innovative "safe space" where migrants can scan and upload their ID, educational or medical records that might get lost during their journey or might not be convenient to keep them physically with them. The lack of documentation is often a key issue in the migratory process.

* GPP App will provide the user with a detailed and comprehensive mapping of solidarity structures in transit/destination countries: upon voluntary geolocalization, an interactive map will provide information on the structures (i.e. associations, collectives, unions, NGOs, lawyers, humanitarian protection) and also up-to-date information on the legislation in force in every country and territory crossed.

* GPP is also a multimedia tool for mixed migrant to report and document abuses faced along the journey after being provided with a brief tutorial on citizen journalism.

The platform is designed WITH migrants rather than FOR migrants: they are the main and ultimate beneficiaries of this project, whose aim is to enable them to embark in safer journeys and experience an easier settling, but also to engage them as active subjects of participatory democracy practices and a narrative process that will start from their first hand experiences as narrating subjects rather than narrated ones.

It is meant to serve as an innovative tool also for the third sector (NGOs, aid agencies) to access information and first-hand data that go beyond government control and a useful tool to improve and strengthen their interventions. GPP may also contribute to an in-depth reconsideration of the operational modalities which are very often blamed for adopting a top-down approach. The possibility to receive detailed information and to be able to directly get in contact with their targets and potential beneficiaries will allow to improve the effectiveness and efficiency of their actions, and ensure a streamlined use of the resources.

## Team

* Clara Capelli is an economic development expert formerly based in the Middle East and North Africa (MENA) region. For GPP she will take care of business development and scalability of the project.
* Antonio Dibattista is a software developer with twenty years' experience in developing apps with a wide range of tools and software languages and he is highly competent on mobile app software. He will develop the IT structure and implement its operativity.
* Pasquale Francavilla is a product owner and full-stack developer with ten years of experience in web development. He's a payment integration expert with a technical and business analysis background gained in banking and fintech domains.
* Stefano Baldassarre is a front-end developer both the web and mobile fields with many years of experience. He will develop the project frontend both on the web and mobile side.
* Maria Tavernini is an independent field researcher and communication expert who has been based in India for the past eight years. For GPP, she will coordinate the editorial work, mapping of solidarity structures and migration routes. 
* Alessandro Di Rienzo has followed Middle Eastern events, labour disputes and migration issues as a journalist and as social mediator. For Global Passport Project he will take care of relations with municipalities and participatory democracy processes.
* Giuseppe Ottaviano is a citizen journalism expert, he is the communication manager at different NGOs working on migration. He will be in charge of communication, press office and marketing 
* Francesco Delia is a professional photographer and videomaker. For the GPP, he takes care of the development of the self-narration video tutorials for migrants and will provide graphic identity
* Elena De Filippo is professor of Sociology of Migrations at the Faculty of Sociology of the Federico II University of Naples, President of the Dedalus Social Cooperative. 
The members of Kosmopolis Association will be in charge of different and specific articulations and needs of the project.

## The Technology

We plan to use the following technologies:

 - Node.js, Loopback4, Typescript, PostgreSQL (back-end)
 - Angular 9, CoreUI, Typescript (front-end)
 - React Native, Typescript, DECode App (mobile app)
 - Restroom, Sawtooth, IPFS (blockchain)

## The Repos

###  GPP_backend
 - [GPP_backend](https://github.com/LedgerProject/GPP_backend)
 - ***GPP_backend*** contains most of the business logic: JWT authentication strategy, write and read data in the database, does cryptography on chunks files with zenroom, expose endpoints needed by front-end and mobile app.
 - It requires Node.js 8.9 or above and PostgreSQL 13 or above.
 - This repository is needed by GPP_frontend.

###  GPP_frontend
 - [GPP_frontend](https://github.com/LedgerProject/GPP_frontend)
 - ***GPP_frontend*** frontend for GPP staff and third sector operators. Allows the display of wallets by a token and the management of the organizations and information displayed on the mobile application.
 - It requires Angular 9 or above.
 - It connects to GPP_backend to call the available endpoints.

###  GPP_app
 - [GPP_app](https://github.com/LedgerProject/GPP_app)
 - ***GPP_app*** mobile application for GPP available for Android and iOS with four main functionalities: the "DocWallet", "AroundMe", "AbuseAlarm" and "News&Stories" sections.
 - It requires React Native.
 - It connects to GPP_backend to call the available endpoints.

## Service Portal

The third sector operator service portal is available at the following link:

[Global Passport Project - Service Portal](https://www.gppadmin.org)

You can register as third sector operator and try how work the portal or login with these demo credentials:

Name: John Doe
E-Mail: operatorgpp@intuizionicreative.it
Password: start2021!

## Mobile Application

The mobile application is available at the following link:

[Google Play Store](https://play.google.com/store/apps/details?id=com.kosmopolis.gpp)

You can register as user and try how work the mobile application or login with these demo credentials:

Name: Mary Doe
E-Mail: usergpp@intuizionicreative.it
Password: start2021!
Answers:
Where did your parents meet?  Paris
What is your home town?       Naples
What is your favorite dish?   Pizza

## Website

The Global Passport Project website is available at the following link:

[Global Passport Project - Website](https://www.globalpassportproject.org)
