# ModJWT


- Required PHP 5.5++ and MODx 2.6++
- This package using Firebase/JWT from https://github.com/firebase/php-jwt



## A MODx extra to works with JSON Web Token (JWT)

Documentation: https://github.com/lokamaya/modJWT (next on this)

Bugs and Feature Requests: https://github.com/lokamaya/modJWT/issues

Discussions and Questions: [MODx Community](https://community.modx.com/t/modjwt-an-extra-to-works-with-json-web-token-jwt/330?u=lokamaya)

This extra is now available on MODx repository that can be downloaded from MODx manager.

----

### Installation

* Download this extra from MODx manager
* Install modJWT
* After successfull installation: go to the default context in modx manager, find and edit sample page /modjwt/
* Then go to system settings > modjwt. There are some default configuration like: Secret Key, Private Key, and Public Key. 

Sample pages contain 1 HTML resource and 3 JSON pages. You can play around with it.

----

### Writing RSA Key

*Note: don't add passphrase*

    ssh-keygen -t rsa -b 4096 -m PEM -f jwtRS256.key
    openssl rsa -in jwtRS256.key -pubout -outform PEM -out jwtRS256.key.pub
    cat jwtRS256.key
    cat jwtRS256.key.pub
