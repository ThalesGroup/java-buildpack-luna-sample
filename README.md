A REST-ful sample application that exercises the Luna HSM.  

To do this, it exposes four cryptography REST endpoints that expect to recieve a JSON payload. Each endpoint returns values that can be used as arguments to the other endpoints.

* `POST /encrypt` - `message`, a message to encrypt.
* `POST /decrypt` - `cipher-text`, a base64 encoded encrypted message to decrypt.
* `POST /sign` - `message`, a message to sign.
* `POST /verify` - `message` and `signature`, a signature to verify against a message.

In addition to these, two information endpoints are exposed.

* `GET /key-pair` - Returns the base64 encoded private and public keys.
* `GET /security-providers` - Lists all of the installed Java security providers.
