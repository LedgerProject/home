# Shared repos and middleware

Here are the info about the components shared by different Ledger teams collaborating as well as middleware components designed to be embedded in third party products. 

## Keypairoom

A Component to generate and regenerate a keypair, in a deterministic and private way. The cryptographic part consists of two [Zenroom](https://github.com/dyne/Zenroom) smart contracts, the first executed server-side to generate a seed (based on public data such as user name), the second generate client side, based on the output of the first smart contract and on private information, namely "The challenges".

The component is in TypeScript and packaged a npm.
 
 - Source: [Keypairoom](https://github.com/LedgerProject/keypairoom)
 - Demo with GUI: [Keypairoom Demo](https://github.com/LedgerProject/keypairoom-demo)
 - Package: [npm](https://www.npmjs.com/package/@dyne/keypairoom) 

## ZenroomBrowserExtension

Web extensions encapsulating Zenroom functionality, written in python and JavaScript. Repo: [ZenroomBrowserExtension](https://github.com/LedgerProject/zen-web-ext).

## Arduino2IPFS

ESP32 Arduino library for submitting data to IPFS. Requires ArduinJSON. Repo: [Arduino2IPFS](https://github.com/LedgerProject/Disemin-ipfs-client-esp32).