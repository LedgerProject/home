# The ConDIDI Project

ConDIDI will develop the full lifecycle for digital event credentials. Our first application is to allow event participants to easily demonstrate their level of involvement at educational events like conferences or workshops, using the technology of self-sovereign identity and verifiable credentials. However this technology is not restricted to events only, instead it can be used for any kind of credentials.


## The Technology

We are building on the SSI framework already developed by Jolocom, that uses ledger technologe to secure the credentials. The frontend and backend are built with ReactJS and Python, the SSI microservice is built with the Jolocom SSI SDK, the session management is using Redis as datastore and the user and event management is using ArangoDB. We plan to take advantage of the graph capabilities of ArangoDB to organise the complex relationships between events, credentials, event participants and organisers. The whole system is separated into modules that interact, i.e. issuing a ticket is done by the frontend doing an api call to the backend, which in turn interacts multiple times with the SSI microservice and the recipients smart wallet on the phone. 


## The Repos

### ConDIDI_frontend
- [ConDIDi_frontend](https://github.com/LedgerProject/ConDIDI_frontend/)
- React app, can be hosted on a webserver

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

