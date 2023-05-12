Getting Started
- To get started writing the ransomware, we will be using the cryptography library:
$ pip install cryptography

There are a lot of encryption algorithms out there. This library we will use is built
on top of the AES algorithm.
Open up a new file, call it ransomware.py and import the following:
- import pathlib, os, secrets, base64, getpass
- import cryptography
- from cryptography.fernet import Fernet
- from cryptography.hazmat.primitives.kdf.scrypt import Scrypt

Don't worry about these imported libraries for now. I will explain each part of the
code as we proceed.
Deriving the Key from a Password
First, key derivation functions need random bits added to the password before
it's hashed; these bits are often called salts, which help strengthen security and
protect against dictionary and brute-force attacks. Let's make a function to
generate that using the secrets module [Link text Here](https://https://docs.python.org/3/library/secrets.html)