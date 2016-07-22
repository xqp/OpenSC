[![Travis CI Build Status](https://img.shields.io/travis/frankmorgner/OpenSC/contactless.svg?label=Travis%20CI%20build)](https://travis-ci.org/frankmorgner/OpenSC) [![AppVeyor CI Build Status](https://img.shields.io/appveyor/ci/frankmorgner/OpenSC/contactless.svg?label=AppVeyor%20build)](https://ci.appveyor.com/project/frankmorgner/OpenSC) [![Coverity Scan Status](https://img.shields.io/coverity/scan/4026.svg?label=Coverity%20scan)](https://scan.coverity.com/projects/4026)

# OpenSC for Contact-Less Smart Cards

This is a fork of [OpenSC/OpenSC](https://github.com/OpenSC/OpenSC/) that includes some features usefull for communication with contact-less smart cards. The extended features include:

- **Smart Card Support**:
  - *Initial support German ID card*:
    - Use eSign for electronic signature (PKCS#11, Minidriver, Tokend)
    - Use PIN management tool for electronic identification (eID)
- **Better File Caching**:
  - Use the contact-less UID allowing to cache certificates *and* metadata from the card
  - Automatic caching with `use_file_caching = true` in `opensc.conf` allows caching during Windows login
- **Generic features for easier integration of new cards**:
  - Generic Secure Messaging encoding according to ISO 7816-8
  - Secure Messaging establishment with Extended Access Control (EAC):
    - Password Authenticated Connection Establishment (PACE)
    - Terminal Authentication (TA)
    - Chip Authentication (CA)

Most of the above features are still open for integration into OpenSC ([OpenSC/OpenSC#831](https://github.com/OpenSC/OpenSC/pull/831), [OpenSC/OpenSC#804](https://github.com/OpenSC/OpenSC/pull/804)). Since review cycles are long and the incentive of the project owner for integration is low, I don't expect to see them to be adopted very soon.
