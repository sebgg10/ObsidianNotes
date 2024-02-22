## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso al nivel
**Usuario:** bandit15
**Contraseña:** jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución

```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 20 17:50:06 2024 GMT; NotAfter: Feb 20 17:51:06 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEIivS1jANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIwMTc1MDA2WhcNMjQwMjIwMTc1MTA2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC4
XC9dgne8ha9I/vXn4uTtObLhI/PPyLyl4jyDQPp61VtsEMcOb95KhXxdtQiDtzSD
3KXQVFLaPlVGKDWSR9nV+GoazSNPmNLH/IMVrUYxXjYikPxo1jjYKyuqfjV5bNm3
Hz6z4eDl7wNbPRaPAMPo0WU23m9M04bKQHLINfN7Abz3a+7ChLeICrWXiXp9mWfj
PY8cK7Vayz0eHU4Lg64q4jUaXQqZ/ta1RqZEwv7ZuTKctcazpK/u2+h4zvQCPyLh
uDjUXZTLlIuhfjyKUJLQsmYHAQprV6sY3ybFN32dW6MSE0/ApT6Th0LzKeaYxk5b
3NIeaYyPeKsjqFSwy+2zAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBQ
RXG1k+cB357X43fsiyaCQQh4RbWHOcg1jBes5eiC/H8MyC3ec1znXvOUfqJcWNQJ
9UJDMwbkpo+IcwJiOe9n/D3Zeypv1g+ta8KKLsQ+zcbp5RdltKy7GuO/s5WjVofE
/IHz/5g+IMoqqYLlquQ539CZykPMC9TB9uWfJj/i8faCox4gjtkSCri+27tUZuHi
eYR3zxY1ptsJti/pMaItC6Oc2/pSlotQ4fXdciLZYGXqlmSFBt8Y8/v1YkhME5gN
3HmBV/Zg1SghA57zYsbf3npvQwudr04f2iF493pe0VRN6DfiXTxWkJe1VKuyGHEr
Q4L4OdVlgMSeyYyKgFc7
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 98C1691BB237C8759F9BDB89230B1032433F0D0C67EF6D48A6F2910E0BCB377F
    Session-ID-ctx:
    Resumption PSK: 977FCD05C4B83EA5A4C11BE85C4BA6998D5C6E562F8D0B9FD6938A9DE8B5D662AAFFB92BA33B60D72157E9CEA65F5068
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 c9 7a 81 90 61 a2 44-6e 83 ab 39 4b a2 9f d6   ..z..a.Dn..9K...
    0010 - 19 33 1c ed 9c e1 a7 c4-5d e4 a8 54 5b c5 34 01   .3......]..T[.4.
    0020 - ff 49 60 bf f5 d9 c1 61-d0 1a d5 77 28 c0 0f 6f   .I`....a...w(..o
    0030 - 90 8a a2 6f 2d ee 14 db-dd e8 9c 7d 21 05 a2 ac   ...o-......}!...
    0040 - 27 ff 7f 7b af fa f3 fc-d8 80 b0 4a f1 78 f4 fc   '..{.......J.x..
    0050 - 9e 31 df 16 b5 86 0c e1-36 4f 4f 78 f7 5f 3c 1c   .1......6OOx._<.
    0060 - 47 1b 2e b5 36 75 50 a1-9f 12 2a bf d8 83 ae 90   G...6uP...*.....
    0070 - 2d 23 34 54 66 9c 4a 8b-6d a9 42 00 85 00 04 46   -#4Tf.J.m.B....F
    0080 - af b0 0f 43 2b d9 16 24-b7 49 fd 21 ba be 0a bb   ...C+..$.I.!....
    0090 - b5 f3 27 1a 6c 32 e8 1b-40 3e d3 17 56 e4 08 ca   ..'.l2..@>..V...
    00a0 - 07 4f 78 e9 98 ba 25 05-79 78 15 ee 91 87 75 91   .Ox...%.yx....u.
    00b0 - 56 b5 ce 11 1a 1f f6 e5-f2 50 40 77 d4 fd fd 83   V........P@w....
    00c0 - 12 ee e7 55 80 b7 33 d0-46 9b cc 17 10 c2 26 c3   ...U..3.F.....&.

    Start Time: 1708457387
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 8FB42856334A39C3B3154FE22F889C2CCD5D0C4BF577AE3FE090AC8F7467C45B
    Session-ID-ctx:
    Resumption PSK: 9552D62A26D97F87D9EA26C2A72F252E8F6D06083A2491C4D5595610C8B27A30443EE520A4A32970834E9F8ABABBE925
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 c9 7a 81 90 61 a2 44-6e 83 ab 39 4b a2 9f d6   ..z..a.Dn..9K...
    0010 - 74 23 66 74 28 09 3c 89-60 76 c2 5a ff b4 bb df   t#ft(.<.`v.Z....
    0020 - 5b 6f 05 a9 8a ec 87 63-1b 94 46 f5 00 2c d9 c0   [o.....c..F..,..
    0030 - 46 25 c7 06 64 63 60 87-df 1c 4d e8 f3 a0 39 a6   F%..dc`...M...9.
    0040 - 3e 30 81 ec 5b 40 1c 72-b2 ef 56 0d 85 c8 80 f5   >0..[@.r..V.....
    0050 - d9 79 15 89 07 b7 3a 69-7f 7b 78 f7 73 a6 1c 74   .y....:i.{x.s..t
    0060 - 9b e1 30 06 75 34 8d 7f-54 b0 68 98 d6 5c 8b 81   ..0.u4..T.h..\..
    0070 - be 5d d5 a1 f5 37 b0 51-49 11 71 84 8c 91 9d 3d   .]...7.QI.q....=
    0080 - 5a 2d dc 2e 02 ab 57 b2-ce 4d 88 82 03 67 52 bb   Z-....W..M...gR.
    0090 - f2 10 6d 26 46 f2 8a 6e-53 c7 07 45 c2 44 22 ae   ..m&F..nS..E.D".
    00a0 - f4 49 5d 4e f9 32 e0 94-2d 93 90 f5 3d 47 0c a1   .I]N.2..-...=G..
    00b0 - 93 f7 b7 33 51 cd a6 9c-40 e5 ed dd 0b 3f 77 e9   ...3Q...@....?w.
    00c0 - c7 27 dc 5c 2d 1d 83 84-d3 1d 7a 66 e9 05 b8 7e   .'.\-.....zf...~

    Start Time: 1708457387
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
```
## Notas adicionales
## Referencias