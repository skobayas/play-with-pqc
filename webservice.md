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

[Web service](https://u80c6yk8og.execute-api.ap-northeast-1.amazonaws.com/default/gen-raw-keypair)

Change : method change GET to POST
(23.Apr)

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

Update :
But you can't use it as usual such as CSR generation, etc.
In general, asymmetric keys are handled special format, it called pkcs#8.
Thus, need such feature.

Update : Added feature "gen-wrap-privatekey"
Also you need to POST, you can get private key with pkcs#8.
[Web service](https://u80c6yk8og.execute-api.ap-northeast-1.amazonaws.com/default/gen-wrap-privatekey)

You will get json.
The value is base64 encoded, it is private key as pkcs#8.

Should I add pre-amble and post-amble?
Yes, I will add it in next update!
