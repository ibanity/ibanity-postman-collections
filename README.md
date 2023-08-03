# Postman collections for Ibanity products

## Covered products

* Ibanity XS2A
* Ibanity Isabel Connect
* Ibanity Ponto Connect

## Setup

1) import the collection(s) into Postman
2) Create Postman env
3) Configure the client certificates in Postman linked to your application

### Postman env

#### Global variables, cross products

* `ibanity-hostname`: the Ibanity API hostname (eg: api.ibanity.com)
* `signatureKey`: the private key for signing request (RSA ...), encrypted with a password
* `signatureKeyPassphrase`: the password of the private key
* `signatureKey`: the signing certificate id. This can be found in "serialNumber" in the signing certificate DN

#### Ponto Connect

* `ponto-authorization-host`: the Ponto authorization URL (eg: authorization.myponto.com)
* `ponto-connect-client-id`: the client-id from your Ponto Connect app that you can find in your Ibanity Developer Portal app
* `ponto-connect-client-secret`: related secret
* `ponto-connect-redirect-uri`: the pre-registered URL where Ponto should send the customer, after authorization (eg: https://postman.local)

#### Isabel Connect

* `isabel-connect-client-id`: the client-id from your Isabel Connect app that you can find in your Ibanity Developer Portal app
* `isabel-connect-client-secret`: related secret

#### Codabox Bankconnect

* `codabox-bankconnect-client-id`: the client-id form your Codabox BankConnect app that you can find in your Ibanity Developer Portal app
* `codabox-bankconnect-client-secret`: related secret

#### Codabox Connect

* `codabox-connect-client-id`: the client-id form your Codabox Connect app that you can find in your Ibanity Developer Portal app
* `codabox-connect-client-secret`: related secret
