[![Travis CI Build Status](https://img.shields.io/travis/frankmorgner/OpenSC/contactless.svg?label=Travis%20CI%20build)](https://travis-ci.org/frankmorgner/OpenSC) [![AppVeyor CI Build Status](https://img.shields.io/appveyor/ci/frankmorgner/OpenSC/contactless.svg?label=AppVeyor%20build)](https://ci.appveyor.com/project/frankmorgner/OpenSC) [![Coverity Scan Status](https://img.shields.io/coverity/scan/4026.svg?label=Coverity%20scan)](https://scan.coverity.com/projects/4026)

# OpenSC for Contact-Less Smart Cards

This is a fork of [OpenSC/OpenSC](https://github.com/OpenSC/OpenSC/) that includes some features usefull for communication with contact-less smart cards. The extended features include:

- **Smart Card Support**:
  - *Support German ID card*:
    - Use eSign for electronic signature (PKCS#11, Minidriver, Tokend)
    - Use PIN management tool for electronic identification (eID)
  - *Smartcard-HSM*:
    - Use Manufacturer PKI for verifying the card and establishing SM
    - Support for [Bundesdruckerei System-on-Card architecture](https://www.bundesdruckerei.de/en/3867-cebit-bundesdruckerei-exhibits-employee-id-card-tomorrow)
    - Support for recovering the authentication status by verifying a session PIN
- **Secure On-Card-Authentication**:
  - Fingerprint verification on-card
  - PIN verification on-card
- **Generic features for easier integration of new cards**:
  - Generic Secure Messaging encoding according to ISO 7816-8
  - Secure Messaging establishment with Extended Access Control (EAC):
    - Password Authenticated Connection Establishment (PACE)
    - Terminal Authentication (TA)
    - Chip Authentication (CA)
  - Support for Session PIN generation according to [Smart Card Minidriver Specification, v7.07](http://download.microsoft.com/download/3/3/2/332FD70B-F04D-470A-A135-040350B9563F/sc-minidriver_specs_v7.07.docx)

Most of the above features are still open for integration into OpenSC ([OpenSC/OpenSC#831](https://github.com/OpenSC/OpenSC/pull/831)). Since review cycles are long and the incentive of the project owner for integration is low, I don't expect to see them to be adopted very soon.
