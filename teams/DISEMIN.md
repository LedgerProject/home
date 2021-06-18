![AgroXM Logo](https://agroxm.com/wp-content/uploads/2020/12/logo.png)

# AgroXM · A Distributed Secure Smart Farming Log

_also known as project **DISEMIN**_


Ex Machina is an IoT system integrator that serves industrial customers with environmental monitoring & predictive analytics solutions, using machine learning and own modular hardware.
We aspire to build an environmental / weather / agriculture data marketplace where farmers and businesses can share data and consume services in a fair manner. Our IoT solution addresses typical precision agriculture requirements, with DLT powered IoT hardware. The sensor data are stored to immutable decentralized file system and made available to blockchain smart contracts, enabling services such as parametric weather crop insurance or data sales to be conducted in an economic and trustless manner. 

Core components and open-source deliverables of MVP:

1. IoT Sensor Node, extended to store sensor data in IPFS
2. IoT PaaS, extended with various custom features to satisfy project goals with end user web dashboards, rule engine for 3rd system integrations, etc.
3. Middleware API / IPFS / CHAINLINK adapter to handle DLT related operations
3. Android mobile application integrated to IoT PaaS, that acts as a front-end for the end user / farmer on the go
4. Smart Contract Factory & Marketplace, that implements a parametric weather crop insurance protection service.


## The Repos

You can find the detailed architecture, the full collection of the solution's code repositories, and guides for running all the components here:
https://github.com/LedgerProject/disemin-home

## Demo

A demo setup of the AgroXM solution has been deployed for the sake of the Ledger project.

- The IoT PaaS is running here: [http://agro.exm.gr:9090](http://agro.exm.gr:9090)

- The IoT PaaS middleware application is running here: [http://agro.exm.gr:3000](http://agro.exm.gr:3000/swagger-ui/index.html?configUrl=/v3/api-docs/swagger-config#/)

- The IPFS middleware API is running here: [http://agro.exm.gr:3001](http://agro.exm.gr:3001/)

- The smart contracts factory frontend application is running here: [http://agro.exm.gr](http://agro.exm.gr)

- You can find binary apk files of the Android app on the repo's [releases page](https://github.com/exmgr/disemin-android/releases). You can also subscribe to Firebase distribution [here](https://appdistribution.firebase.dev/i/eb2c04a656c76602) in order to receive future app updates. The demo credentials for logging in the android app (or the IoT platform) are:

```
username = demo@exm.gr
password = demo123
```

## Attribution 

Built using open source software, with the help of the Ledger EU project and their fantastic people!

![Ledger Logo](../media/general/LedgerLogo.png)
