# The  Project

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

SafePKT technology consists of a web based frontend and server-side backend which work
together to provide a software developer with reports about potential bugs or security
issues in their code.

SafePKT depends on the following technologies:
 - Node.js, Typescript, Vue.js, NuxtJs (front-end)
 - Rust, Docker engine, Rust Verification Tools, LLVM, KLEE (back-end)

## The Repos

SafePKT consists of two separate components:
 - the [SafePKT backend](https://github.com/LedgerProject/safepkt_backend) leveraging 
    - the [Rust Verification Tools](https://github.com/project-oak/rust-verification-tools),
      - the [KLEE Symbolic Execution Engine](http://klee.github.io/)
    - the [Docker Engine](https://www.docker.com/)
 - the [SafePKT frontend](https://github.com/LedgerProject/safepkt_frontend) based on [NuxtJS](https://nuxtjs.org/)

A [third repository](https://github.com/LedgerProject/safepkt) has been created to ease both
 - installation of the project and
 - contribution to it.

