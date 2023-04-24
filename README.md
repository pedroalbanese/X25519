# X25519 NIST SP800-186
[![ISC License](http://img.shields.io/badge/license-ISC-blue.svg)](https://github.com/pedroalbanese/X25519/blob/master/LICENSE.md)
[![GitHub downloads](https://img.shields.io/github/downloads/pedroalbanese/X25519/total.svg?logo=github&logoColor=white)](https://github.com/pedroalbanese/X25519/releases)
[![GoDoc](https://godoc.org/github.com/pedroalbanese/X25519?status.png)](http://godoc.org/github.com/pedroalbanese/X25519)
[![Go Report Card](https://goreportcard.com/badge/github.com/pedroalbanese/X25519)](https://goreportcard.com/report/github.com/pedroalbanese/X25519)
[![GitHub go.mod Go version](https://img.shields.io/github/go-mod/go-version/pedroalbanese/X25519)](https://golang.org)
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/pedroalbanese/X25519)](https://github.com/pedroalbanese/X25519/releases)

X25519 is an elliptic curve Diffie-Hellman key exchange using Curve25519. It allows two parties to jointly agree on a shared secret using an insecure channel.

```
            Alice                        Bob
            -----                        ---
       choose private key          choose private key
             d_A                         d_B
              |                           |
              v                           v
        compute public key:        compute public key:
  Q_A = d_A * BasePoint_Mont   Q_B = d_B * BasePoint_Mont
              |                           |
              v                           v
           ----- Begin Key Exchange Phase -----
              |                           |
              v                           v
        compute shared secret:     compute shared secret:
 S_A = Montgomery(Q_B * d_A)   S_B = Montgomery(Q_A * d_B)
              |                           |
              v                           v
            ----- End Key Exchange Phase -----
              |                           |
              v                           |
            (S_A)                       (S_B)
```

### Command-line X25519 Diffie-Hellman Tool:
<pre>Usage of x25519:
  -key string
        Private key.
  -keygen
        Generate ed25519 asymmetric keypair.
  -pub string
        Remote's side Public key.</pre>

### Examples:
```sh
./x25519 -keygen // 2x
./x25519 -key $2ndprivatekey -pub $1stpublickey
./x25519 -key $1stprivatekey -pub $2ndpublickey
```
## License
This project is licensed under the ISC License.
##### Copyright (c) 2020-2021 Pedro Albanese - ALBANESE Research Lab.
