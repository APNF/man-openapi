# man-openapi

[![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

Welcome to the APNF MAN platform API reference.

The OpenAPI files present in this repository provide to API clients the necessary information to access the APIs made available by the MAN platform, the STIR/Shaken french solution for service providers, and operated by the APNF (ASSOCIATION DES PLATEFORMES DE NORMALISATION DES FLUX INTER-OPERATEURS).

The APIs are split into 3 main categories:
- Authentication API
- GCO (Gestionnaire des Certificats Opérateurs) API
- BPCO (Base Publique des Certificats Opérateurs) API

If you are a service provider operating in France, you need to be registered as an APNF member in order to get access to the MAN platform and be able to get STI certificates.
If you are not yet a member, please contact the APNF.


## MAN Platform API
> [apnf-man-platform-openapi.yaml](apnf-man-platform-openapi.yaml) / (View in [Swagger Editor](https://editor.swagger.io/?url=https://raw.githubusercontent.com/apnf/man-openapi/main/apnf-man-platform-openapi.yaml))

MAN platform APIs to create and manage users, credentials, STI certificates and
all other objects that service providers can handle on the MAN platform.

More information is available in the OpenAPI file itself.


## Authentication API
> [apnf-man-platform-openapi-auth.yaml](apnf-man-platform-openapi-auth.yaml) / (View in [Swagger Editor](https://editor.swagger.io/?url=https://raw.githubusercontent.com/apnf/man-openapi/main/apnf-man-platform-openapi-auth.yaml))

This API reference details the method to get access tokens required for authenticating against MAN platform GCO API methods.

More information is available in the OpenAPI file itself.


## GCO API
> [apnf-man-platform-openapi-gco.yaml](apnf-man-platform-openapi-gco.yaml) / (View in [Swagger Editor](https://editor.swagger.io/?url=https://raw.githubusercontent.com/apnf/man-openapi/main/apnf-man-platform-openapi-gco.yaml))

This API reference explains how to get access to MAN platform functionalities related to the creation and management of STI certificates to be used by service providers for signing their SIP telephone calls per the STIR SHAKEN protocol.

This API is a subset of the [MAN Platform API](apnf-man-platform-openapi.yaml)

More information is available in the OpenAPI file itself.

## BPCO API
> [apnf-man-platform-openapi-bpco.yaml](apnf-man-platform-openapi-bpco.yaml) / (View in [Swagger Editor](https://editor.swagger.io/?url=https://raw.githubusercontent.com/apnf/man-openapi/main/apnf-man-platform-openapi-bpco.yaml))

This API reference enumerates the public APIs to used by service provider STI-VS components to retrieve and validate STI certificates.


## BND API
> [apnf-man-platform-openapi-bnd.yaml](apnf-man-platform-openapi-bnd.yaml) / (View in [Swagger Editor](https://editor.swagger.io/?url=https://raw.githubusercontent.com/apnf/man-openapi/main/apnf-man-platform-openapi-bnd.yaml))

This API reference explains how to manage display delegations and associated functionalities.

This API is a subset of the [MAN Platform API](apnf-man-platform-openapi.yaml)

More information is available in the OpenAPI file itself.

# Licensing

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0
International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
