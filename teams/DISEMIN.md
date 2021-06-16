![AgroXM Logo](https://agroxm.com/wp-content/uploads/2020/12/logo.png)

# AgroXM · A Distributed Secure Smart Farming Log

_also known as project **DISEMIN**_


Ex Machina is an IoT system integrator that serves industrial customers with environmental monitoring & predictive analytics solutions, using machine learning and modular hardware.

Like most Greeks, we have farmers in our family and we see that the farming digital transformation promise is derailing.  We see farmers losing control over their farming practices, becoming alienated from their work and having to adjust to technology and large corporations rather than the other way round.

To address the farm data sovereignty issues, we are introducing **AgroXM**, an open IoT solution for smart agriculture, aiming to become a data marketplace where farmers and advisors can share data and services in a fair manner.

## The Technology

We are providing a complete open source IoT solution that combines a farmer's log mobile application with crop sensor data and weather forecasts, using a distributed ledger built into the hardware, and a marketplace that will enable farmers and advisors to collaborate.

## The Repos

_**TL;DR** You can find the detailed architecture, the full collection of the solution's code repositories, and guides for running all the components [here](https://github.com/LedgerProject/disemin-home)._

## Components

![Architecture](https://raw.githubusercontent.com/LedgerProject/disemin-home/main/media/architecture.jpg)

The solution consists of multiple modules:

#### IoT Platform

The IoT platform is a fork of the multi-starred open source project [Thingsboard](https://github.com/thingsboard/thingsboard). It facilitates the entire process of provisioning sensor devices, sending their measurements to the cloud, and finally post-processing and visualizing the data.

The IoT platform runs on Java and the data store in a PostgreSQL database, and can run on any machine, from a RPi to any modern OS (Linux, Windows, MacOS). It can also deployed using docker, as microservices.

#### IoT Hardware Node

Our node is an energy and communication autonomous IoT sensor node with weather sensors, that stores sensor data directly to IPFS and automates execution of parametric weather insurance contracts on-chain via the distributed chainlink oracle system.

The node is open source, both software (firmware) and hardware, and is written in Arduino.

#### IoT Platform Middleware

The middleware is essentially a proxy server that exposes a REST API, hiding the complexity of the IoT platform's own REST API, facilitating multiple use cases. Typically, such use cases involve batching operations that would require multiple REST API calls into one call, authentication, failover and rollback mechanisms.

The middleware runs on Java. It's very lightweight and can be run in parallel with the IoT platform.

#### IPFS Middleware

The PFS middleware is a backend application that takes care of all the necessary file operations, after the IoT sensor node stores a file on IPFS. It acts as a lightweight HTTP server that listens for requests from the sensor node. As its primary purpose, once it receives an IPFS CID from a sensor node, the middleware performs all the required IPFS file operations. The sensor node only needs to use a single HTTP API call.

The IPFS middleware is writen in Node.js and can be deployed using docker.

#### Android App

The Android app is the end-user interface of the whole system. It communicates with the middleware and acts both as a farmer's log, where the farmer can manually input activities and other field-related notes, as well as a full farm monitoring solution, where the farmer can view data from the weather stations and/or other sensors that are deployed in the field.

#### Web App

The Web application is a front-end application for the farmer, allowing for the creation of a parametric insurance contract on Ethereum, based on weather conditions acquired from IPFS through a Chainlink node.

The web app is written in React / Node.js and can be deployed using docker.

#### Other

The solution also requires a running Chainlink node and a running IPFS node.

#### Read More

You can read more about each module in their respective repos.

## Demo

A demo setup of the AgroXM solution has been deployed for the sake of the Ledger project.

- The Thingsboard IoT platform is running here: [http://agro.exm.gr:9090](http://agro.exm.gr:9090)

- The platform middleware application is running here: [http://agro.exm.gr:3000](http://agro.exm.gr:3000/swagger-ui/index.html?configUrl=/v3/api-docs/swagger-config#/)

- The IPFS middleware application is running here: [http://agro.exm.gr:3001](http://agro.exm.gr:3001/)

- The web frontend application is running here: [http://agro.exm.gr](http://agro.exm.gr)

- The Android app is currently distributed using Firebase Distribution and can be downloaded [here](https://appdistribution.firebase.dev/i/eb2c04a656c76602). The demo credentials for logging in the android app (or the IoT platform) are:

```
username = demo@exm.gr
password = demo123
```

## Attribution 

Built using open source software, with the help of the Ledger EU project and their fantastic people!

![Ledger Logo](../media/general/LedgerLogo.png)
