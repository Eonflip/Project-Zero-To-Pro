# RSA Algorithm

The RSA ("Rivest-Shamir-Adleman") Algorithm is a widely used and popular asymmetric cryptographic algorithm that encrypts and decrypts data.

This algorithm is utilized to transfer sensitive data.

## Why RSA?

This algorithm's strength comes from the concept that you can multiply 2 large prime numbers together rather easily, BUT factoring that same large number is very difficult.

## How does it work?

RSA is a public and private key pair algorithm. The way this works is simple, you give out a public key to those who want to send you data, whilst you hold the private key. The public key encrypts the data and the private key decrypts the data. This means that while encrypting should be fairly straightfoward and known publicly, the decryption process should be much more difficult. 

- Encryption: To encrypt the data the formula is: $$\text{cipertext} = m^e \bmod n$$

  
- Decryption: To decrypt the data the formula is: 