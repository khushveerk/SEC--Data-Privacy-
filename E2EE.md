# Elliptic Curve Cryptography (ECC)
ECC is an approach to public key cryptography. It’s main benefit is that keys are very small compared to, say, RSA.

ECC uses elliptic curves over finite fields. “Finite field” just means that values are, well, finite. Think modular arithmetic; basically values on the curve are modulo’d after calculation so that they loop back over the same finite set of values rather than approaching + or - infinity.

read the reference for understanding elliptic curves better 
## reference - 
https://medium.com/@philipshen13/monero-part-1-key-concepts-3671186016c6


## Diffie-Hellman-Merkle Key Exchange
Diffie-Hellman-Merkle (DHM) key exchange protocol, which enables 2 users to create a shared secret key (for symmetric cryptography) over a public channel. It is what enables stealth addresses, which Monero uses to hide the receivers of transactions.

<img width="1059" height="1568" alt="Image" src="https://github.com/user-attachments/assets/713598e8-b029-43b1-be96-c7bd4eb36df8" />

