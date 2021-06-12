# The  Project

**YouChoose is a browser extension which allows users to see YouTube recommendations from the content creator they are watching.**

*Problem:*

70% of the content watched on YouTube is selected by YouTube's algorithms. These systems are designed to maximize the interests of the platform, ie generate clicks and ad-revenue. 

As a result, YouTubers who invest a lot of efforts into creating quality content, have their audience pushed towards more clickbaity or sensationalist content, because the algorithm assesses that the click-trough rate would be marginally higher. 

Users end up having their attention hijacked into watching attention-catching content which provides them with little value.

*Solution*:

Our tool empowers internet users over platforms to control online recommendations.  

We beleive that content creators are in a better position to recommend the most relevant videos to watch after their own content that an AI with miasligned incentive. 

YouChoose will enable content creators to pick a selection of videos they want to recommend after each of their own videos, which will be displayed on the recommendation sidebar of all users with the extension installed. 

Our project will be developed as a non-profit, with a collective governance model which will include the content creators which will take part in the project.


* The main tool revolve around a browser extension and the intention of hijack people attention from youtube.
* giving control back to content creator is 
* Our stack is nodejs and mongodb. For ledger we want to design an infrastructure with less single point of failures

## The Technology

1. Creating a browser extension to change youtube UX, initially based on hardcoded information. 

2. Gradually integrate with a centralized backend implemented in nodejs and mongodb. Implement backup, redundancy, caching, and CDN for this server. Perform stress testing and evaluate decentralized models. Considering the data are not personal, we might likely think to adopt also DHT or ipfs for content distribution and to avoid SPoF. 

3. Creating an interface for content creators where they can select and control their recommendations requires a javascript web framework to implement an understandable and usable UX.

Although point 1 might sound straightforward, and Youtube allows extension that enhances the experience but has already cracked down extension, they might impact their business model. We are slightly worried about this possibility; therefore we want to focus on making it most robust and reliable, and then, we have a few: "Optional nice to have," technical components:

* Study a wrapping website for the mobile experience and onboard people (Eventually analyze and integrate technology from on invidio.us approach on how to wrap youtube videos reliably.)
* Integrate a micropayment model by integrating a few components of Metamask extension into ours.

We would like to talk about these possibilities, as they the are strategic for the success of YouChoose, but we do not want to commit in tasks that might be excessive hard for the 6 months.

## The Repos

Write 2 lines about your different repos 
Write 2 lines about your different repos 

### Generic_backend
 - [Zenroom](https://github.com/dyne/zenroom)
 - ***Zenroom*** Crypto VM for blockchain and databases
 - Makes coffee
 - Makes candyfloss
 
### Generic_frontend
 - [DECODE APP](https://github.com/dyne/decode-proximity-app)
 - ***DECODE App*** React-native app, built for cryptography
 - Makes pizza
 - Makes fries
