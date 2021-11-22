# /e/ - Privacy Central app

/e/ is an Android operating system which respect its users’ privacy!

That is why, as part of the LEDGER program, we are developing a “Privacy Central app”. This app will let Android users have a good understanding of the privacy concerns that exist around applications they are using. And, in addition, it will give them tools to protect their privacy.

For the LEDGER project, we focus mainly on two features:
1. Tracker blocker: this feature lets the user see, analyse and block trackers in apps
1. IP scrambling: this features lets users hide their IP

## The Technology

### Tracker blocker

The tracker blocker relies on a local DNS proxy in order to analyse and block DNS requests.

### IP scrambling

We will use the Tor network in order to let users hide their IP.

## The Repos

The project relies on multiple repositories

**Main application**

https://github.com/LedgerProject/e_privacycentral_privacycentralapp

**Modules**

-	https://github.com/LedgerProject/e_privacycentral_privacymodulesapi
-	https://github.com/LedgerProject/e_privacycentral_privacymodulese
-	https://github.com/LedgerProject/e_privacycentral_privacymoduletor
- https://github.com/LedgerProject/e_privacycentral_privacymoduletrackerfilter

**DNS resolver**

https://github.com/LedgerProject/e_privacycentral_android_system_netd

