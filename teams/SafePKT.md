# The  Project

Check out the SafePKT official website: https://safepkt.cjdns.fr/

SafePKT is a project to study and build static analysis technology for the Rust code
used in the PKT project. PKT is a project for disintermediating telecom monopolies by
de-coupling the roles of infrastructure operation from (internet) service provision.
PKT uses a blockchain based on the bitcoin protocol and a proof of work algorithm called
PacketCrypt which requires bandwidth in order to mine. The vision of PacketCrypt is to
drive investment into network infrastructure by creating artificial demand for
bandwidth.

You can find out more about the overall PKT project by going to: https://pkt.cash/

In the SafePKT project we are focused on improving software development efficiency
(and therefore time to market) for software used within the PKT ecosystem
(e.g. PacketCrypt / cjdns). As security breaches in cryptocurrency software often lead to
irrecoverable loss, such projects have higher than normal security requirements. However
in this innovative and competitive space, time to market is also a critical to a project's
overall success. With the help of cutting edge research in the academic space, we are
developing improved software verification tools which will be easier to use and more helpful
to developers who will apply them to improving software development efficiency and security
in projects within the PKT ecosystem.

## The Technology

The technology of PKT overall includes [PacketCrypt](https://pkt.cash/PacketCrypt-2020-09-04.pdf)
bandwidth-hard proof of work, [Lightning Network](https://en.wikipedia.org/wiki/Lightning_Network),
and [cjdns](https://github.com/cjdelisle/cjdns) networking protocol.

SafePKT technology consists of a web based frontend and server-side backend, which work
together to provide a software developer with reports about potential bugs or security
issues in their code.

Both a [command-line (CLI) application](https://github.com/LedgerProject/safepkt_backend/releases) and a [Visual Studio Code plugin](https://marketplace.visualstudio.com/items?itemName=CJDNS.safepkt-verifier) offer independently from the two previous components,  
reports containing the same level of detail offered by the backend when it comes to  
analyzing a rust-based smart-contract written on top of [Parity's ink! eDSL](https://github.com/paritytech/ink/tree/v2.1.0) - see https://github.com/paritytech/ink/tree/v2.1.0.

SafePKT depends on the following technologies:
 - Single-page application:
   - [Node.js](https://nodejs.org/),
   - [Typescript](https://www.typescriptlang.org/),
   - [Vue.js](https://vuejs.org/),
   - [NuxtJs](https://nuxtjs.org/)
 - Server-side back-end and rust command-line application:
   - [Rust](https://www.rust-lang.org/),
   - [Docker engine](https://www.docker.com/products/container-runtime),
   - [Rust Verification Tools](https://project-oak.github.io/rust-verification-tools/),
   - [LLVM](https://llvm.org/),
   - [KLEE](http://klee.github.io/)
 - Node.js command-line application:
   - [Node.js](https://nodejs.org/),
 - SafePKT assertion library:
   - [Rust](https://www.rust-lang.org/),
 - VS Code extension:
   - [Got](https://github.com/sindresorhus/got/tree/v11.8.2),
   - [Tree-sitter](https://tree-sitter.github.io/tree-sitter/),
   - [Typescript](https://www.typescriptlang.org/),
   - [VS Code Extension API](https://code.visualstudio.com/api)

## The Repos

SafePKT consists of three separate components:
 - a [backend](https://github.com/LedgerProject/safepkt_backend) leveraging 
   - the [Rust Verification Tools](https://github.com/project-oak/rust-verification-tools),
   - the [KLEE Symbolic Execution Engine](http://klee.github.io/),
   - the [Docker Engine](https://www.docker.com/).  
   This backend offers capabilities to verify program written in Rust,  
   by emitting LLVM bitcode, consumed by KLEE Symbolic Execution Engine.  
   Besides it provides developers and researchers with two separate execution modes:
   - HTTP verification with a REST API,  
   - CLI (Command-Line Interface) verification.  
 - a [frontend](https://github.com/LedgerProject/safepkt_frontend) based on [NuxtJS](https://nuxtjs.org/),  
 - a secondary [CLI (command-line application)](https://github.com/LedgerProject/safepkt_cli) based on [Node.js](https://nodejs.org/),  
 - an [assertion library](https://github.com/LedgerProject/safepkt_assert) based on [rvt verification annotations library](https://github.com/LedgerProject/safepkt_rust-verification-tools/tree/main/verification-annotations),  
 - a [ready-for-verification smart contract project example](https://github.com/LedgerProject/safepkt_smart-contract-example),  
   based on [one of ink! eDSL examples: a Plain Multisig Wallet](https://github.com/paritytech/ink/tree/v2.1.0/examples/multisig_plain),
 - an [extension for Visual Studio Code](https://github.com/LedgerProject/safepkt_vscode-plugin),
 - and at last but not least, [a research paper](https://github.com/LedgerProject/safepkt_paper) "On the Termination of Borrow Checking for Rust" authored by
   - [Etienne Payet](etienne.payet@univ-reunion.fr),
   - [David Pearce](david.pearce@ecs.vuw.ac.nz) and
   - [Fausto Spoto](fausto.spoto@univr.it)

A [fourth repository](https://github.com/LedgerProject/safepkt) has been created to ease
 - automation of compilation and publication (from GitHub) of the [research paper](https://github.com/LedgerProject/safepkt_paper/releases)
 - [installation](https://github.com/LedgerProject/safepkt#install) of the project frontend, backend and CLI components and
 - [contribution](https://github.com/LedgerProject/safepkt#contribute) to those components, along with maintenance of the VS Code extension

## Demo

An online demo of a rust-based smart contract verification is available from
 - [https://safepkt.cjdns.fr](https://safepkt.cjdns.fr)

Rust-based smart contract analysis and verification is also available to developers and
researchers by installing [VS Code](https://code.visualstudio.com/download) and [SafePKT Verifier extension](https://marketplace.visualstudio.com/items?itemName=CJDNS.safepkt-verifier)
from VS Code Marketplace.
 - [https://marketplace.visualstudio.com/items?itemName=CJDNS.safepkt-verifier](https://marketplace.visualstudio.com/items?itemName=CJDNS.safepkt-verifier)

## Contact

### GitHub

 - [Caleb James de Lisle](https://github.com/cjdelisle)
 - [Étienne Payet](https://github.com/etiennepayet)
 - [David Pearce](https://github.com/DavePearce)
 - [Fausto Spoto](https://github.com/spoto)
 - [Thierry Marianne](https://twitter.com/thierrymarianne)

### LinkedIn

 - [David Pearce](https://www.linkedin.com/in/david-pearce-8592647/)
 - [Fausto Spoto](https://www.linkedin.com/in/fausto-spoto-65171/)
 - [Thierry Marianne](https://twitter.com/thierrymarianne)

### Twitter

 - [Caleb James de Lisle](https://twitter.com/cjdelisle)
 - [David Pearce](https://twitter.com/WhileyDave)
 - [Thierry Marianne](https://twitter.com/thierrymarianne)

