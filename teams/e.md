# /e/ - Privacy Central app

/e/OS is a deGoogled and pro-privacy mobile operating system compatible with Android applications!

That is why, as part of the LEDGER program, we are developing a “Privacy Central app”. This app will let Android users have a good understanding of the privacy concerns that exist around applications they are using. And, in addition, it will give them tools to protect their privacy.

For the LEDGER project, we focus mainly on two features:
1. Tracker blocker: this feature lets the user see, analyse and block trackers in apps
1. IP scrambling: this features lets users hide their IP

## The Technology

### Tracker blocker

The tracker blocker relies a customized DNS resolver. For each request, it checks if the DNS domain is in the blocking list. We also implemented a mechanism to whitelist an app, if for any reason a user doesn't want to block all (or a given) trackers on this app.

In addition, it records all requests for the blocked domains, in order to provide stats for the user.

### IP scrambling

The application connects the device to the Tor network (using the Android implementation, Ortbot).

## The Repos

The project relies on multiple repositories

**Main application**

The Android application project contains the 4 main features of the app:
- Trackers: see, analyse and block trackers
- IP Scrambling: hide the real IP of the device
- Fake Geoloc: hide the real location of the device
- Permissions: manage application permissions

https://github.com/LedgerProject/e_privacycentral_privacycentralapp

**Modules**

The application is based on multiple modules to make the code easier to maintain, and it also offers opportunities to improve the support on other devices

-	https://github.com/LedgerProject/e_privacycentral_privacymodulesapi: the API used by the application
-	https://github.com/LedgerProject/e_privacycentral_privacymodulese: the implementation of the API for /e/ devices
-	https://github.com/LedgerProject/e_privacycentral_privacymoduletor: the components for IP Scrambling
- https://github.com/LedgerProject/e_privacycentral_privacymoduletrackerfilter: the components for Tracker Blocker

**DNS resolver**

Finally, the Tracker filter module works with a customized DNS resolver, embedded within the OS. This project need to be build with /e/

https://github.com/LedgerProject/e_privacycentral_android_system_netd

## Demo

If you want to test the demo, please contact us at testing@e.email.

To be informed about the release of the Privacy Central project within /e/OS, please [subscribe to our newsletter](https://e.foundation/contact-e-2/#my-anchor1).

For any other question, feel free to contact rikviergever@e.email.

---

[eFoundation](https://e.foundation/) | [Newsletter](https://e.foundation/contact-e-2/#my-anchor1) | [eSolutions](https://esolutions.shop/) | [Forum](https://community.e.foundation/) | [Documentation](https://doc.e.foundation/) | [eCloud](https://ecloud.global/)
