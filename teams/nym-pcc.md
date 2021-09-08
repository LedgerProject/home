# Nym Private COVID Certificate (PCC) 

The existing Digital Covid Certificates (including the European DCC) do not provide strong privacy properties. They can expose unnecessary information about an individual and are not resistant to forgery if the underlying cryptography is compromised. Worse, they can further be used to create a map of the places the person has visited and therefore be used as a tracking system. 

We propose a privacy enhanced version using blinded and re-randomizable Coconut credentials that can tackle the above issues. We call this product **Private Covid Certificate (PCC)**. PCC is an extension of Nym's Digital Identity system which also uses Coconut as the underlying technology.  


## Technology

Privacy is provided by [Nym's Coconut technology](https://github.com/nymtech/coconut), both for identity and private versions of documents that contain large amounts of personal data, e.g. COVID passes and test results.

The mobile app prototype has been developed as a [Progressive Web App (PWA)](https://web.dev/progressive-web-apps/) using [React](https://reactjs.org/) to avoid the need to deploy it via the Google Play or Apple App Stores. This saves on the long review cycles, deployment complexity and makes it easy to try out without installing an app.

In the future, the prototype app can be adapted to use [React Native](https://reactnative.dev/) so that it can be built into a native app and release via the normal app stores for Android and iOS.

The mobile app uses the following key libraries:

- [React](https://reactjs.org/), 
  [Webpack](https://webpack.js.org/), 
  [Babel](https://babeljs.io/),
  [Typescript](https://www.typescriptlang.org/) and 
  [React Material UI](https://material-ui.com/).
- [HTML5 Audio and Video capture](https://www.html5rocks.com/en/tutorials/getusermedia/intro/) for device camera access.
- Health certificate decoding libraries and forks from European Union's Digital Green Certificate efforts via the [European eHealth network](https://github.com/ehn-dcc-development).
- [Tesseract.js](https://tesseract.projectnaptha.com/) and [`mrz`](https://www.npmjs.com/package/mrz), to OCR and decode the Machine Readable Zones of documents such as passports.

## Repo

https://github.com/LedgerProject/nym-pcc

