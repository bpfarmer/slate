---
title: API Reference

language_tabs:
  - shell
  - swift
  - java
  - go
  - ruby
  - python

toc_footers:
  - <a href='#'>Sign Up for Beta Access</a>

includes:
  - errors

search: true
---

# Introduction

How can we make cryptography usable for the consumer? How can we make it easier for developers to build secure systems?

Key aims to answer these questions by providing usable, decentralized public key management and libraries to simplify signatures and encryption.

We hope to see: better authentication, end-to-end encrypted communication, cryptographically-verifiable statements and contracts, author-signed content, and encrypted file-sharing and backups. 

Client code examples are provided for iOS, Android and cURL, and backend service examples are written in Go, Ruby and Python.

We hope that this will encourage developers to create an Internet that is more secure and more free.  

# Getting Started

## Picking a Provider

First, we pick a **Public Key Provider**. Providers on Key do the hard work involved with managing, sharing and verifying public keys. We'll use the [Sandbox](https://sandbox.k3y.io) for now.

We connect to Providers through a REST API, and receive a response either as a JSON array or a Protocol Buffer. We can register a public key, request a public key, or efficiently audit a Provider through the API.

Let's retrieve a user's public key in the browser: [/test_user/keys/1.json](https://sandbox.k3y.io/test_user/keys.json). 

We can see the user's X.509 certificates and the Provider's proof that the keys are valid.

## Using a Client

> Using the Key Demo Client

```shell
  git clone https://github.com/keycx/demo.git
  cd demo
  python simple_encrypt.py
```

Next, we have to set up a **Client**, which generates, stores and verifies public keys, and encrypts and signs data.

For this example, we'll use a simple shell client written in Python. Clone the source [here](https://github.com/keycx/demo.git), then browse to the source: `$ python simple_encrypt.py`

### Registering

Through the client, we generate a Public/Private Keypair and register the public key with the Sandbox Provider. We retrieve a signed commitment from the Provider that our public key has been accepted. 

### Encryption

```shell
  Username > echo
  
  Message > 'Some message here'
  
  Decrypted response is 'Some message here' 
```

There's a user in the Sandbox named Echo. Let's get her public key from the Sandbox and verify it. Type `echo` into the client.

Now that we have her valid public key, we can encrypt a message. Type anything into the prompt, and we'll encrypt using our keypair and her public key.

### Decryption

Now, we'll listen for messages in return. Echo decrypts received messages, then she repeats them and encrypts her own message to the sender.

# Providers

With Key, users don't have to manually verify public keys, a major barrier to usability. Providers issue public key bindings that are efficiently monitored by the user and by a network of decentralized auditors. 

## Creating a Provider

Providers can be hosted independently or through Key. Providers are monitored to ensure that public key bindings are correct, 

## Auditing a Provider

## Whistleblowing

# Clients

Anything that has an Internet connection, secure storage for private keys, and computational power for cryptographic operations with side-channel resistance can be a Key **Client**. Clients create keypairs, store private keys, register and retrieve public keys, and encrypt and sign data. Further, Clients audit their own public-key bindings to ensure that the **Provider** isn't serving false keys. 

## Keypairs

Key uses 

## Registering a Public Key

## Auditing your Public Key

## Verifying a Public Key

## Adding a New Device

# Encryption

# Signatures

# Authentication

## Why Key?

## Registration

## Logins

## Proof-of-Identity

# Acknowledgments

Key owes a great deal to the following people and organizations, who have developed many of the technologies that we use.

- [Certificate Transparency](https://www.certificate-transparency.org/)
- [CONIKS](https://eprint.iacr.org/2014/1004.pdf) developed by Marcela S. Melara, Aaron Blankstein, Joseph Bonneau, Edward W. Felten, Michael J. Freedman
- [NaCl](http://nacl.cr.yp.to/) developed by Daniel J. Bernstein

[1]: http://coniks.org "Based on the CONIKS project developed by Marcela Melara, Aaron Blankstein, et al"

