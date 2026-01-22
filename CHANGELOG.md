# Changelog

## 1.7.1 - 2025/06/05

- (BPCO) (Certificates) Update serial_number min size limit to 16 characters
- (GCO) (Certificates) Update serial_number min size limit to 16 characters
- (GCO) (Certificates) GET /certificates - add `provider_code` property as allowed sort criteria
- (GCO) (Certificates) Add `issuer_dn` and `renewed_by` in certificate data model
- (PTF) (Certificates) Update serial_number min size limit to 16 characters
- (PTF) (CallTraces) GET /calltraces - new query parameters `provider_disengagement`, `exclude_self_author` and `search_type`
- (PTF) (Certificates) GET /certificates - add `provider_code` property as allowed sort criteria
- (PTF) (Certificates) Add `issuer_dn` and `renewed_by` in certificate data model
- (PTF) (Meteo) Increase `long_description` maximum size for meteo event from 1000 to 5000 characters
- (PTF) (Providers) GET /providers/referential - give access to supervisor users
- (PTF) (Providers) GET /providers/referential - add technical number in CSV response
- (PTF) (Providers) GET /ticket - add `modification_date` property as allowed sort criteria
- (PTF) (Tickets) New GET /ticket/export API to export tickets
- (PTF) (Tickets) `author_ticket_internal_id` is now updatable
- (PTF) (Tickets) new properties available in data model

## 1.7.0 - 2024/09/09

- New Open API file for APNF MAN Platform - Platform API Reference
- (AUTH) Reorder alphabetically components
- (BPCO) Reorder alphabetically components
- (GCO) (Certificates) Add `INVALIDATION` status to be used during CA compromission
- (GCO) (Certificates) New API method - GET /certificates/export
- (GCO) (Providers) GET /providers/{provider_id}/bypass_token - Rename response from `records` to `bypass_tokens`
- (GCO) (Providers) Remove users and history API methods as available as part of the **MAN Platform API Reference** document.
- (GCO) (Providers) Cleanup provider unused examples and schemas

## 1.6.1 - 2024/04/30

- (GCO) (Certificates) Update `renewal_after` property description - certificate renewal delay is based on certificate validity start date

## 1.6.0 - 2023/12/13

- (BPCO) (Description) Fix spelling error in 'Rate limiting'
- (BPCO) (History) Set correct 1.5.1 version for 2023/10/05 release

- (GCO) (Certificates) PATCH /certificates/{certificate_id} - Add constraints for expired certificates
- (GCO) (Certificates) POST /certificates/{certificate_id} - Add 409 HTTP status case
- (GCO) (Certificates) GET /certificates/export - New endpoint to export certificates as CSV
- (GCO) (Providers) GET /providers/{provider_id} - New `legal_administrator` property to provide provider current legal administrator user.
- (GCO) (Providers) GET /providers - Removed `verified`, `verified_at` and `verified_status` filters as never implemented
- (GCO) (Providers) GET /providers/{provider_id}/bypass_token - Add 415 HTTP status case
- (GCO) (Providers) PATCH /providers/{provider_id} - New `legal_administrator` property to change provider legal administrator user
- (GCO) (Providers) PATCH /providers/{provider_id} - Allow `opts_contracts` property to be edited by MANAGER users
- (GCO) (Providers) Add `BypassTokenId` schema
- (GCO) (Providers) Update `BypassToken` schema to add `BypassTokenId` reference and specify required properties
- (GCO) (Providers) Update `bypass_token` property in `Provider` schema
- (GCO) (Providers) Remove `domains_allowed` mentions from `ProviderCreationRequest` schema and examples as property has been removed since 1.3.0 release
- (GCO) (Providers) Updated `ProviderDetails` schema to add `deposit_notification_list` property and remove `last_verification` property
- (GCO) (Users) GET /users - Add `created_at`, `updated_at` and `last_connected_at` properties to `UserSummaryView` schema
- (GCO) (Users) GET /users - Grant API method access to the MANAGER role.
- (GCO) (Users) GET /users/{user_id} - Grant API method access to the MANAGER role.
- (GCO) (Users) GET /users/{user_id} - New `legal_administrator ` to see if user is legal administrator.
- (GCO) (Users) POST /users – Allow APNF administrators to create provider administrator users
- (GCO) (Users) PATCH /users - Allow APNF administrators to update the role of any provider user.
- (GCO) (Users) POST /users/reset-credential - Rename original reset-password to enhance functionality by adding reset of OTP and resend new link of account activation.
- (GCO) (BPCO) GET /bpco/certificates - Add missing `Content-Length` response header
- (GCO) (Description) Fix spelling error in 'Rate limiting'

## 1.5.1 - 2023/10/05

- (BPCO) (GET /ca) Update `version` format from integer to float
- (BPCO) (GET /ca/certs) Update `version` format from integer to float

## 1.5.0 - 2023/09/27

- (AUTH) Clarify access token lifetime
- (AUTH) Include in `Description` section rate limiting logic
- (AUTH) Add CC-BY-SA-4.0 license
- (BPCO) Include in `Description` section rate limiting logic
- (BPCO) Add CC-BY-SA-4.0 license
- (GCO) Include in `Description` section rate limiting logic
- (GCO) Add CC-BY-SA-4.0 license

## 1.4.0 - 2023/06/27

- (GCO) (Providers) GET /providers/{provider_id} - Add `bypass_token` property in Provider schema
- (GCO) (Providers) GET /providers/{provider_id}/bypass_token - Add new API to generate a new provider bypass token
- (GCO) (Providers) POST /providers/{provider_id}/bypass_token - Add new API to retrieve latest generated provider bypass token

## 1.3.0 - 2023/06/16

- (AUTH) Add `servers` entries for VABF and Preproduction platforms
- (AUTH) Update `client_assertion` value in example request body
- (AUTH) Update `access_token` value in example response body
- (AUTH) Describe format of the `access_token` generated in the response
- (BPCO) Add `servers` entries for VABF and Preproduction platforms
- (BPCO) (GET /ca) Clarify format for `version` and `sequence` properties
- (BPCO) (GET /ca) Remove `byte` format for response body properties as they are Base64 URL encoded and not Base64 encoded.
- (BPCO) (GET /ca/certs) Clarify format for `version` and `sequence` properties
- (BPCO) (GET /ca/certs) Remove `byte` format for response body properties as they are Base64 URL encoded and not Base64 encoded.
- (GCO) Add `servers` entries for VABF and Preproduction platforms
- (GCO) (Certificates) Clarify `renewal_after` property usage
- (GCO) (Certificates) Clarify `valid_to` constraints
- (GCO) (Providers) Deprecate `domains_allowed` property
- (GCO) (Providers) `technical_number` property cannot be edited by provider administrators


## 1.2.0 - 2023/05/04

- (AUTH) Replace `token_type` response 'bearer' value to 'Bearer'
- (AUTH) Update response body required properties and add `refresh_expires_in` and `scope` properties
- (AUTH) Add 405 error case
- (AUTH) Update `error_description` example value for 400 error case
- (BPCO) Add 405 HTTP status case to all responses
- (BPCO) Add 409 HTTP status code to the Common Error Codes section
- (BPCO) Add `Content-Type` header to all 4xx HTTP status cases
- (BPCO) (GET /certs/{spc}/{sn}.cer) Add 400 HTTP status case
- (BPCO) (GET /crl) Add `Content-Type` header for 304 HTTP status case
- (BPCO) (GET /crl) Remove `Content-Length` header for 304 HTTP status case
- (BPCO) (GET /ca) Add `Content-Type` header for 304 HTTP status case
- (BPCO) (GET /ca) Remove `Content-Length` header for 304 HTTP status case
- (BPCO) (GET /ca/certs) Add `Content-Type` header for 304 HTTP status case
- (BPCO) (GET /ca/certs) Remove `Content-Length` header for 304 HTTP status case
- (BPCO) (GET /ca/certs/{sn}.cer) Add 400 HTTP status case
- (BPCO) (GET /ca/crl) Add `Content-Type` header for 304 HTTP status case
- (BPCO) (GET /ca/crl) Remove `Content-Length` header for 304 HTTP status case
- (GCO) Remove `Content-Length` header for 204 and 304 responses
- (GCO) Update error message for 401 HTTP responses
- (GCO) Add 405 HTTP status case + update error message
- (GCO) Use different ID values depending on the object type
- (GCO) (Certificates) Add new status `INVALID`
- (GCO) (POST /certificates/) Add `updated_at`, `updated_by` properties to response examples
- (GCO) (POST /certificates) Add `Location` header in responses
- (GCO) (POST /certificates/) Test certificates cannot have the `renewal_auto` property enabled.
- (GCO) (PATCH /certificates/{certificate_id}) Test certificates cannot have the `renewal_auto` property enabled.
- (GCO) (POST /certificates/{certificate_id}/renew) Add constraints for revoked and invalid certificates
- (GCO) (POST /certificates/{certificate_id}/renew) Test certificates cannot have the `renewal_auto` property enabled.
- (GCO) (POST /certificates/{certificate_id}/renew) Clarify valid_from/valid_to property constraints
- (GCO) (POST /certificates/{certificate_id}/renew) Add 409 HTTP status case for revoked certificates
- (GCO) (POST /certificates/{certificate_id}/renew) Add `Location` header in responses
- (GCO) (POST /certificates/{certificate_id}/revoke) Add constraints for expired, revoked and invalid certificates
- (GCO) (HEAD /bpco/certificates) Remove `Content-Length` response header and body
- (GCO) (GET /bpco/certificates) Add `Content-Type` header for 304 HTTP status case
- (GCO) (HEAD /bpco/crl) Remove `Content-Length` response header and body
- (GCO) (GET /bpco/crl) Add `Content-Type` header for 304 HTTP status case
- (GCO) (Providers) New `deposit_notification_list` property in Provider object
- (GCO) (Providers) Improve `domains_allowed` property description for `ProviderCreationRequest` example
- (GCO) (Providers) Allow `opts_contracts` property to be edited by *ADMINISTRATOR* users
- (GCO) (Users) New `/users/{user_id}/preferences` method
- (GCO) (Users) Remove `/user/activate` method


## 1.1.0 - 2023/01/18

- (AUTH) Update API URL to prefix path with *auth/*
- (AUTH) Update `aud` property description to add *auth/* in its possible values and use a reference to the document `servers.url` property
- (BPCO) Update base URL from *https://man-bpco.fr/* to *https://api.man-bpco.fr/*
- (GCO) Update base URL from *https://man-plateforme.fr/api/* to *https://api.man-plateforme.fr/*
- (GCO) Update BPCO API URLs from *https://man-bpco.fr/* to *https://api.man-bpco.fr/*
- (GCO) Change `Certificate` component schema to change `revoked_at` property format from `integer` to `string`
- (GCO) Update certificate serial number schema pattern
- (GCO) Cleanup `ProviderOIDCSettings` component schema

## 1.0.0 - 2022/09/28

Initial Release
