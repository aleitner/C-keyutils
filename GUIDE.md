# Using the Lightning Keys Utilities Library

This library enables creating keys, retrieving public keys, creating the SIN, and signing payloads.

## Quick Start
### Installation

Clone the github repository and include the lightningKeys.h header in your project. This should give you access to the functions:

```c
int generatePem(char **pem) // creates an ECKEY and sets the value of pem to the PEM encoding of the key
int getPublicKeyFromPem(char *pemstring, char **pubkey) //takes a pem string and sets the value of pubkey to the compressed public key extracted from the pem
int generateSinFromPem(char *pem, char **sin) //gets the base58 unique identifier associated with the pem
int signMessageWithPem(char *message, char *pem, char **signature) //sets signature to the signature of the sha256 of the message
```

## Running the Tests

```bash
$ sh build.sh
```
