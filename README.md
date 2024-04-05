# What is this?
Trivial samples play with PQC

## Why am I writing such page?
Several samples are partial.
I am looking for full operation samples,
but didn't find such ones.

## For example?
According to several material, private and public key size of Dilithium2 are 2528 and 1312.
Yes, some of plain implementation generates key pair which size are same.
It seemed to raw key.
On the other hands, I got a key from OQS-OpenSSL which size is 3870.

In general, we use asymmetric key as certificates.
Thus, should prepare CSR(Certificate Singing Request).

But could not generate CSR from above raw keys.
Of course, OQS-OpenSSL can generate CSR and keys which size is different.

Yes I understand the differences with dumping keys.

## Does it the reinvent wheel?
Must be yes.
But, extend this, I will have full samples for PQC operations.
