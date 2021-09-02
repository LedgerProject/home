# The  Project

Media and digital content creators are in the midst of a transformation. On the one hand, traditional media, which used to live from paper printing, have had to transition to the digital model. Due to the pandemic situation, their off-line revenues have decreased drastically; so, they are looking for new revenue models and have not found a fair and sustainable business model.

Newspapers were selling their pages to print advertising on them. Since the Internet was born, media, publishers and other content creators have not found a fair and sustainable business model. Today they are still doing the same thing but, in digital format, counting page views. On the other side, users annoy ads, cannot privately pay on the Internet, and there are no validations to buy restricted content (i.e. age-restricted content ).

Currently, users who consume content have to navigate through annoying websites full of advertisements, or if they want to access paid content, they have to sign up for subscriptions when they really only want to read one or two articles. This is an increasing problem and content creators need alternative revenue streams. That is why we are introducing moncon, a pay-for-content method that allows users to pay a few cents for what they want to consume, without subscriptions. This will also allow content creators to continue working on creating quality content.

With micropayments, users can pay a few cents to read an article, which helps the content creator to focus on creating quality content. The payment is private and validates user data like age, gender, city or any other verifiable credential using Zero-Knowledge Proof.
To solve that problem, there is no other technology available but Blockchain: visa micropayments are expensive and always you do an online payment you have to share your personal data. Our solution, moncon, helps us to make micropayments using Interledger protocol (based on Ripple) while keeping the user privacy using Zero-Knowledge Proof with verifiable credentials, following the W3C standard of Web Monetization and SSI model being GDPR compliance by default, using Zenroom, in that case. 


## The Technology

###	Backend: 
-	express: used for the creation of the API REST  and socket.
-	Interledger: open platform that makes it easy for developers to integrate Open Payments into their applications (first version of PoC we are using Stripe payments because Interledger technology is not ready to go live to the market).
	
### Databases: 
-	MongoDB: where the persistent information necessary for the operation of the platform is stored.
-	MySQL: database used by wordpress.

### Frontend: 
-	ReactJs: library used to create the UI to improve the user experience.
-	Wordpress: for the demo we will use that content management system that can easily use our private micropayments platform.
-	Blockchain integration: used libraries depending on the need web3.

###	Blockchain: 
-	Zenroom and Sawroom: API used to handle and encrypt sensitive user information, allow the use of the Zero Knowledge Protocol, allows information to be shared and verified without revealing unnecessary data, thus maintaining a very high level of security.
-	Interledger: is an open protocol suite for sending payments across different  ledgers. Like the internet, connectors route packets of money across  independent networks. The open architecture and minimal protocol enable  interoperability for any value transfer system.


## The Repos
### Dashboard
- **[See more...](https://github.com/LedgerProject/moncon/tree/main/packages/dashboard)**
- moncon Dashboard is coded in React is designed to provide a content log to block and monetize, as well as metrics for your blocked content. 

### Progressive Web App (moncon Wallet)
-- **[PWA](https://github.com/LedgerProject/moncon/tree/main/packages/moncon-wallet)**
-- moncon wallet is a Progressive Web App fully encoded in React. moncon Wallet is designed to provide verifiable credential issuing and sharing and QR code scanner and micropayments. 

### API
-- **[API](https://github.com/LedgerProject/moncon/tree/main/packages/api)**
-- moncon API is coded in NodeJS and Zenroom, designed to run microservices required by the Dashboard and the progressive web app. 

### Publisher JS
-- **[Publisher JS](https://github.com/LedgerProject/moncon/tree/main/packages/publisherjs)**
-- Publisher JS is a JavaScript libreary with the goal to execute the paywall framework, using a QR code to be able to block the content for specific credentials and sell it at a fix priced. 
