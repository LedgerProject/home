# PATIO

We’ll install solar panels on rooftops in poors neighborhoods in Seville so that the sale of the electricity obtained allows the purchase of local fresh food, helping reduce malnutrition and the local commerce to flourish.

1) For the purchase of these fresh products, families would use a local social cryptocurrency that we’ve already in circulation in this neighbourhood (ILLA). 

2) We’re developing a measurement and invoicing system for solar power production using DLT technology.

We’ll start with a pilot project to evaluate a working solution (MVP) in a local church  with an agreement with Caritas, a global charity ONG. 

Thanks to this project proposal, we’ve recently won (28/06/2021) the social impact acceleration program award from UNICEF Lab.


## The Technology

We'll develop the PATIO device, based on a RPi 3b+ connected to a smart meter to measure the generation, consumption and trade of the energy generated from the solar panels. Blockchains and DLTs are integrated in the system when saving the logs to the IOTA's Tangle to make them immutable and trustable by third parties. As close as possible from the source. Also, the social cryptocoin (ILLA) uses the technology built by FUSE.io on an Ethereum sidechain.

## The Repos

We have one repo for the backend side ()
And other one for the frontend of the dashboard

### PATIO_backend
 - Django app for dashboard's backend
 - System running on the PATIO device to read sensors and send data to backend and IOTA
 
### PATIO_frontend
 - Frontend for the dashboard and/or SaaS
