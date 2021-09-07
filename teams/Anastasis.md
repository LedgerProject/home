# The  Project

Encryption is broadly assumed to allow users to stay in control of
their data, but it merely reduces the problem of safe-keeping a large
amount of data to keeping the encryption key safe.  Keeping keys
available and confidential is thus a crucial problem for informational
self-determination.

Anastasis will allow users to make backups of their keys, utilizing
an open set of backup providers.  During the backup process, these
providers will learn nothing from the protocol: not the identity of
the users, not the keys, not who the other providers are the user
is using, and not even how to authenticate the users.  During key
recovery, the providers will learn the minimum amount of information
required to authenticate the user (like the user's e-mail address
or phone number), but nothing more. Only the user will be able to
recover the key material.  The key material is split over multiple
providers, allowing the user to specify which combinations of
authentication methods should allow key recovery.

Anastasis includes anonymous payment functionality to enable the
providers to offer their service on a commercial basis.


## The Technology

A key idea is to derive an identity key from the user's core
attributes.  Core attributes are information like the user's name,
bithdate, place of birth or social security number. While this
information may be available to strong adversaries, it is not
available to weak adversaries, not disclosed by the protocol to the
providers, and can thus serve as a first layer of protection: the keys
derived from the user's core attributes are used to encrypt the policy
and authentication data that must be stored at the providers.  Even if
a strong adversary is able to break this first layer of security, the
will additionally have to break the multi-factor authentication
challenges set by the user.

Anastasis builds on a set of professionally operated backup providers
that are responsible for performing the authentications. The protocol
allows users to pay for this service, creating an incentive for the
providers to provide a reliable commercial experience.  We use GNU
Taler to support anonymous payments, which is crucial to keep the
user's identity hidden from the providers.

On the cryptographic side, we mostly use a combination of symmetric
encryption (AES+GCM), hashing (HKDF, SHA-512) and expensive hashing
(argon2) to encrypt information, derive key material and prevent
brute-force attacks.  EdDSA is used for signatures to identify
"accounts". This is the only operation that is not already
post-quantum safe, and the place it is used is not crucial for
availability or confidentiality.

We expect have the following dependencies:

 - PostgreSQL (database)
 - libgnunetutil, libsodium (crypto)
 - GNU Taler (payments)
 - GNU libmicrohttpd, libjansson (REST service)
 - External service providers for authentication
 - Postfix (E-mail authentication)
 - Typescript (final front-end)
 - GNU gettext, Jinja2 (internationalization, Web page)



## The Repos

### NGI LEDGER
 - https://github.com/LedgerProject/Anastasis

### Core_logic
 - https://git.taler.net/anastasis.git
 - REST backend, database adapter, authentication plugins,
   reducer-style client-side cryptography
 - Core documentation

### Website
 - https://git.taler.net/anastasis-www.git
 - Web site (https://anastasis.lu/)
 - GNU gettext internationalized  static page generator based on Jinja2

### Gtk+ GUI
 - https://git.taler.net/anastasis-gtk.git
 - Gtk+ based UI prototype
