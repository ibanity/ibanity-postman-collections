# Postman collections for Ibanity products

## Covered products
* Ibanity Codabox BankConnect
* Ibanity Codabox Connect
* Ibanity Isabel Connect
* Ibanity Ponto Connect
* Ibanity XS2A

## Pre-requisites
* You have an account on the Ibanity Developer Portal: https://developer.ibanity.com/
* You have created an application (sandbox or live)
* You have created the `TLS` and `Signature` certificates in the *Credentials* section of your app in the Developer Portal

## Preliminary note
* Those Postman collection are using [Forge - RSA for Postman](https://github.com/loveiset/RSAForPostman) to sign the HTTP request
* *Forge* will be downloaded inside your Postman environment variable at the first request
* *Forge* is quite a big library, and the download may fail at first try. Just retry your request if so

## Setup
1. Import the collection(s)
2. Create environment variables
3. Configure the client (TLS) certificate

### 1. Import the collection(s)
In Postman, use the **Import** button on top left, then choose the provided collection(s)

### 2. Create environment variables
#### Global variables, cross products
* `ibanity-hostname`: the Ibanity API hostname (eg: api.ibanity.com)
* `signatureKey`: the private key for signing request (RSA ...), encrypted with a password
* `signatureKeyPassphrase`: the password of the private key
* `signatureKey`: the signing certificate id. This can be found in "serialNumber" in the signing certificate DN

#### Codabox Bankconnect
* `codabox-bankconnect-client-id`: the client-id form your Codabox BankConnect app that you can find in your Ibanity Developer Portal app
* `codabox-bankconnect-client-secret`: related secret

#### Codabox Connect
* `codabox-connect-client-id`: the client-id form your Codabox Connect app that you can find in your Ibanity Developer Portal app
* `codabox-connect-client-secret`: related secret

#### Isabel Connect
* `isabel-connect-client-id`: the client-id from your Isabel Connect app that you can find in your Ibanity Developer Portal app
* `isabel-connect-client-secret`: related secret

#### Ponto Connect
* `ponto-authorization-host`: the Ponto authorization URL (eg: authorization.myponto.com)
* `ponto-connect-client-id`: the client-id from your Ponto Connect app that you can find in your Ibanity Developer Portal app
* `ponto-connect-client-secret`: related secret
* `ponto-connect-redirect-uri`: the pre-registered URL where Ponto should send the customer, after authorization (eg: https://postman.local)

### 3. Configure the client (TLS) certificate
* Go to Postman **Settings**
* Select **Certificates**
* Add your certificate and private key.
* Hostname is `api.ibanity.com`
* (Don't forget your passphrase)
