# What is this?
An web service which wrapped liboqs-python.

Simple diagram

API_gateway => AWS lambda => liboqs-python

## Does it work?

Yes, but at this time, the feature is very limited.

18.Apr : 
You can get raw keypair of Dilithium2.

## How to use?
Just send GET request to following URL.

Note : It may change without any notice.

[Web service](https://u80c6yk8og.execute-api.ap-northeast-1.amazonaws.com/default/get-raw-keypair)

## I got zip archive which contains two files. Does it work as excepted?

Yes.
That is RAW key pair of Dilithium2.
Both key are base64 encoded, each (binary format) size should be following.

Secret(Private) key : 1312 Byte

Public key          : 2420 Byte

It describe following page.

[dilithium home](https://pq-crystals.org/dilithium/index.shtml)

You can make sure that key pair works as expected with following pages.

[pqc.js](https://dashlane.github.io/pqc.js/)