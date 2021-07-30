# JWT Concepts

## What is JWT?

[JWT](https://jwt.io/) is a standard for the creation of verifiable claims in the form of tokens. 

## Parts of a JWT Token

There are 3 parts to a JWT token:
- The header, which contains metadata about the token such as:
    - Algorithm used to generate the signature
    - Link to a public key to verify the signature
- The payload, which is the json claim
- The signature, which is how the claim is checked

## JWT for Authentication

For authentication, all that is necessary is to verify that the signature is correct.  
The payload can be used to contain the user's name or id, which can be checked against a database.  
If one doesn't care about safety or trusts the token to work completely, they can add access claims to the payload.  
The private key can be any string; I don't currently know how best to store it, so I just keep it in a config file.