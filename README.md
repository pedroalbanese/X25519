# X25519 NIST SP800-186
X25519 is an elliptic curve Diffie-Hellman key exchange using Curve25519. It allows two parties to jointly agree on a shared secret using an insecure channel. 
### X25519 Tool
<pre>Usage of x25519:
  -derive
        Derive shared secret key.
  -key string
        Private key.
  -keygen
        Generate ed25519 asymmetric keypair.
  -pub string
        Remote's side Public key.</pre>

### Examples
```sh
./x25519 -keygen // 2x
```
```sh
./x25519 -derive -key $2stprivatekey -pub $1stpublickey
```
```sh
./x25519 -derive -key $1stprivatekey -pub $2stpublickey
```
## License
This project is licensed under the ISC License.
##### Copyright (c) 2020-2021 Pedro Albanese - ALBANESE Research Lab.
