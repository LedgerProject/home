# The ConDIDi Project

ConDIDi aims to simplify existing solutions regarding employee certification after workshops or trainings using the technology of self-sovereign identity and verifiable credentials. 
Our application unites a hands-on, mobile first approach using a portable and secure Identity SmartWallet in combination with a Webapp usable via Desktop or Smartphone. 

The prototype functionality currently consists of 
* Creation of users (Signing Up + Logging In - both via email and password and via Jolocom SmartWallet)
* Creation of events 
* Adding / Deleting / Managing participants of those events
* Alerting participants via email, supplying them with a QR code to scan in order to get their event tickets
* Allowing the event creator to check-in participants at the events via QR code


## The Technology

We are building on the SSI framework already developed by Jolocom, that uses decentralized ledger technology to secure the credentials. 
The frontend and backend are built with VueJS and Python, the SSI microservice is built with the Jolocom SSI SDK, the session management is using Redis as datastore and the user and event management is using ArangoDB. 

In the future, we plan to take advantage of the graph capabilities of ArangoDB to organise the complex relationships between events, credentials, event participants and organisers. 
The whole system is separated into modules that interact, i.e. issuing a ticket is done by the frontend doing an API call to the backend, which in turn interacts multiple times with the SSI microservice and the recipients smart wallet on the phone. 


## The Repos

### ConDIDI_frontend
- [ConDIDi_frontend](https://github.com/LedgerProject/ConDIDI_frontend/)
- Vue app, can be hosted on a webserver

### ConDIDI_backend
- [ConDIDI_backend](https://github.com/LedgerProject/ConDIDI_backend/)
- python based
- deployable as docker conainer
- docker-compose adds SSI microservice redis and arangoDB containers as data stores
- install.sh for easy installation

### SSI microservice
- [SDK-RPC-Interface](https://github.com/jolocom/sdk-rpc-interface/)
- nodejs based
- deployable as docker container
 
### Prototype
- [Prototype](https://labs.tib.eu/condidi/)
- Prototype deployed in a VM at TIB


## Misc
- [Jolocom SmartWallet](https://github.com/jolocom/smartwallet-app)

