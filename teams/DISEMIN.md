![AgroXM Logo](https://agro.exm.gr/wp-content/uploads/2020/12/logo-300x300.png)

# AgroXM, a Distributed Secure Smart Farming Log

_formerly known as project **DISEMIN**_


Ex Machina is an IoT system integrator that serves industrial customers with environmental monitoring & predictive analytics solutions, using machine learning and modular hardware.

Like most Greeks, we have farmers in our family and we see that the farming digital transformation promise is derailing.  We see farmers losing control over their farming practices, becoming alienated from their work and having to adjust to technology and large corporations rather than the other way round.

To address the farm data sovereignty issues, we are introducing **AgroXM**, an open IoT solution for smart agriculture, aiming to become a data marketplace where farmers and advisors can share data and services in a fair manner.

## The Technology

We are providing a complete open source IoT solution that combines a farmer's log mobile application with crop sensor data and weather forecasts, using a distributed ledger built into the hardware, and a marketplace that will enable farmers and advisors to collaborate.

## The Repos

The solution consists of three modules:

- [disemin-platform](https://github.com/LedgerProject/disemin-platform): a cutting edge IoT platform
- [disemin-middleware](https://github.com/LedgerProject/disemin-middleware): a middleware server application for simplifying client operations with the IoT platform and facilitating the data sharing mechanisms that will be built in the future
- [disemin-android](https://github.com/LedgerProject/disemin-android): a client mobile application for managing the farm's log and accessing all the sensor data

### IoT Platform

The IoT platform is a fork of the multi-starred open source project [Thingsboard](https://github.com/thingsboard/thingsboard). It facilitates the entire process of provisioning sensor devices, sending their measurements to the cloud, and finally post-processing and visualizing the data.

The IoT platform runs on Java and the data store in a PostgreSQL database, and can run on any machine, from a RPi to any modern OS (Linux, Windows, MacOS). It can also deployed using docker, as microservices.

### Middleware

The middleware is essentially a proxy server that exposes a REST API, hiding the complexity of the IoT platform's own REST API, facilitating multiple use cases. Typically, such use cases involve batching operations that would require multiple REST API calls into one call, authentication, failover and rollback mechanisms.

In future versions the middleware will hold all the smart-contract-related code that will facilitate the data marketplace.

The middleware runs on Java. It's very lightweight and can be run in parallel with the IoT platform.

### Android App

The Android app is the end-user interface of the whole system. It communicates with the middleware and acts both as a farmer's log, where the farmer can manually input activities and other field-related notes, as well as a full farm monitoring solution, where the farmer can view data from the weather stations and/or other sensors that are deployed in the field.

You can read more about each module in their respective repo.

## Attribution 

Built using open source software, with the help of the Ledger EU project and their fantastic people!

![Ledger Logo](../media/general/LedgerLogo.png)
