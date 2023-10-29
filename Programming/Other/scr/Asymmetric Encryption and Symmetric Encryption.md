
### Symmetric Encryption

Alice has a file that she wants to send to Bob. However, she wishes no one else but him to see it. She encrypts the file and sends to Bob. But how will she share the key securely with Bob so he might open it?

Asymmetric encryption tries to solve this.

### Asymmetric Encryption

It's comparable to a mailbox that is exposed to anyone who knows its location. We can say that the location of the mailbox is competently

But only the owner of the mailbox has a key to open it up and read messages. So, in this case, both Alice and Bob has to generate a keypair of **Public Key** and **Private Key** on their computers. A popular way to do this is to generate via RSA algorithm. The Public and Private keys generated will be mathematically linked.

Public keys can be used to encrypt data and only the matching private key can be used to decrypt it. The keys cannot be derived from eachother.

In this scenario:

- Both start by exchanging their Public Keys with each other.
- Now Alice can send her sensitive document again.
-  She takes the document and encrypts with Bob's Public Key.
- She sends the file to Bob, who uses his **private** key to unlock the document and read it. 

##### Things that Use this Type of Encryption

- HTTPS websites (SSL)
- SSH
- Bitcoin
- PGP or GPG