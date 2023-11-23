# Metaswitch changelog

The below Changelog is from the APNF branch, from which this is forked. The changes made by Metaswitch (a Microsoft company) to the individual APIs are documented within those files. The versioning in those files is also the Metaswitch versioning and does not match the versions below in this Changelog.

## Version correlation (APNF -> Metaswitch)
- (AUTH): 1.5.1 -> 1.0.0
- (BPCO): 1.5.1 -> 1.0.0
- (GCO): 1.5.1 -> 1.0.0

# Changelog

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
