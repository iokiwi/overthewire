http://overthewire.org/wargames/bandit/

### Excercise 0
http://overthewire.org/wargames/bandit/bandit0.html
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
bandit0
```

### Excercise 1
http://overthewire.org/wargames/bandit/bandit1.html
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
bandit0
```

```bash
cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

Flag: `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`

### Excercise 2
http://overthewire.org/wargames/bandit/bandit2.html

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

Flag: `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`

### Excercise 3
http://overthewire.org/wargames/bandit/bandit3.html
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```

### Excercise 4
http://overthewire.org/wargames/bandit/bandit4.html
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```

### Excercise 5
http://overthewire.org/wargames/bandit/bandit5.html
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
```

```bash
file inhere/*
```
```
inhere/-file00: data
inhere/-file01: data
inhere/-file02: data
inhere/-file03: data
inhere/-file04: data
inhere/-file05: data
inhere/-file06: data
inhere/-file07: ASCII text
inhere/-file08: data
inhere/-file09: data
```

```bash
cat inhere/-file07
the password is koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```

Flag `koReBOKuIDDepwhWk7jZC0RTdopnAYKh`

### Excercise 6
http://overthewire.org/wargames/bandit/bandit6.html
```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```

```bash
ls -laR inhere | grep 1033 -C10
cat inhere/maybehere07/.file2
```

Flag: `DXjZPULLxYr17uwoI01bNLQbtFemEgo7`

### Excercise 7
http://overthewire.org/wargames/bandit/bandit7.html
```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```

```bash
find / -user bandit7 -group bandit6
cat /var/lib/dpkg/info/bandit7.password
```

Flag: `HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs`

### Excercise 8
http://overthewire.org/wargames/bandit/bandit8.html
```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```

```bash
grep "millionth" data.txt
millionth	cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```

### Excercise 9
http://overthewire.org/wargames/bandit/bandit9.html
```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```

```bash
cat data.txt | sort | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

### Excercise 10
http://overthewire.org/wargames/bandit/bandit9.html
```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

```bash
cat data.txt | strings | grep -E -a "=+"
```

### Excercise 11
http://overthewire.org/wargames/bandit/bandit10.html
```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```

```bash
cat data.txt | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPRcd
```


### Excercise 12
http://overthewire.org/wargames/bandit/bandit12.html

```bash
ssh bandit11@bandit.labs.overthewire.org -p 2220
IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```

Flag `5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu`

### Excercise 13
http://overthewire.org/wargames/bandit/bandit13.html
```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```

...

Flag: `8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL`

### Excercise 14
http://overthewire.org/wargames/bandit/bandit14.html

```bash
ssh bandit13@bandit.labs.overthewire.org -p 2220
8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```

```
ssh -i sshkey.private bandit14@localhost
```

```bash
cat /etc/bandit_pass/bandit14
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
```

Flag `4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e`

### Excercise 15
http://overthewire.org/wargames/bandit/bandit15.html

```bash
ssh bandit14@bandit.labs.overthewire.org -p 2220
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
```

```bash
telnet localhost 30000
```

```
Trying 127.0.0.1...
Connected to localhost.
Escape character is '^]'.
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr

Connection closed by foreign host.
```

Flag: `BfMYroe26WYalil77FoDi9qh59eK5xNr`

### Excercise 16
http://overthewire.org/wargames/bandit/bandit16.html

```bash
ssh bandit15@bandit.labs.overthewire.org -p 2220
BfMYroe26WYalil77FoDi9qh59eK5xNr
```


```bash
openssl s_client -connect localhost:30001
```

```
CONNECTED(00000003)
depth=0 CN = localhost
verify error:num=18:self signed certificate
verify return:1
depth=0 CN = localhost
verify return:1
---
Certificate chain
 0 s:/CN=localhost
   i:/CN=localhost
---
Server certificate
-----BEGIN CERTIFICATE-----
MIICBjCCAW+gAwIBAgIEfkeLojANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMTkwODAzMDc0OTMxWhcNMjAwODAyMDc0OTMxWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAMDGwHmT
GntqHvPYiM0wm4Dsmhlmiywaj0CGZKW1Cx6ze9pH+iWXEvcnWga4Kfevqh0LJLeS
jmgE6hFRK9rTwq+q6UE0hADazxb7r8jpthnHwKyRGEtFmsFTv/JqJDk+V5cngA4Y
m4scTjF+r1Y7jQA5VkUPHy+eYoNoqRqGh7JhAgMBAAGjZTBjMBQGA1UdEQQNMAuC
CWxvY2FsaG9zdDBLBglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0
ZWQgYnkgTmNhdC4gU2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3
DQEBBQUAA4GBAEICbhntCy/wyg56HQpox3nt8YtTkr6g21P4akxso7m08u6FuyiY
t/8yd+iph6qlRDHQ+D8T4TcpflsV8YKPXIgMoJQtGkuVgqHeCfgBEJcx+T52F8aX
84l5d7tEr9XEuCPKIlf4/GL8wOQLww2a2+sjlSwa8S1XlkbC61JzPyS3
-----END CERTIFICATE-----
subject=/CN=localhost
issuer=/CN=localhost
---
No client certificate CA names sent
Peer signing digest: SHA512
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1019 bytes and written 269 bytes
Verification error: self signed certificate
---
New, TLSv1.2, Cipher is ECDHE-RSA-AES256-GCM-SHA384
Server public key is 1024 bit
Secure Renegotiation IS supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
SSL-Session:
    Protocol  : TLSv1.2
    Cipher    : ECDHE-RSA-AES256-GCM-SHA384
    Session-ID: E847673D9B777DD3446424EE2FD5A956DBB0D7A52A70EF4DD3A33FE7370141C4
    Session-ID-ctx: 
    Master-Key: C3C05EADCA59DB737E14D408DBC526D9556BBE493FF50210DB65C150F477C600FA5DE954E5F99A8B8B8EAF86D4794D97
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 6a 32 a6 c7 27 26 f0 c8-b4 75 99 96 41 ed a8 13   j2..'&...u..A...
    0010 - 1e ee 5e bb f0 48 bc 96-de ce 8e 5a ba 62 36 07   ..^..H.....Z.b6.
    0020 - 24 fb 29 1e b8 75 df 77-60 8c ea 3b 8b be 33 9f   $.)..u.w`..;..3.
    0030 - c8 89 24 32 13 83 20 a7-c8 12 5d 0a 40 57 52 c1   ..$2.. ...].@WR.
    0040 - 80 57 bf ca f2 50 de ff-66 06 e3 10 ac 21 d1 7e   .W...P..f....!.~
    0050 - c6 da b2 e7 cc e6 0d 61-52 a8 b2 a5 46 4b 64 cd   .......aR...FKd.
    0060 - 75 e5 54 4d c1 63 33 23-0c b4 07 36 ec 49 10 ed   u.TM.c3#...6.I..
    0070 - 1b ff 53 46 f1 6b f2 48-f2 f4 ed d8 11 f5 b3 40   ..SF.k.H.......@
    0080 - 9d d2 6c 42 0f 45 c8 40-ea c7 fe 4f 7b e2 ee 1e   ..lB.E.@...O{...
    0090 - eb 43 88 03 74 1a a7 cd-b3 9d 2e 98 e2 58 65 58   .C..t........XeX

    Start Time: 1564967371
    Timeout   : 7200 (sec)
    Verify return code: 18 (self signed certificate)
    Extended master secret: yes
---
BfMYroe26WYalil77FoDi9qh59eK5xNr
Correct!
cluFn7wTiGryunymYOu4RcffSxQluehd

closed
```

Flag: `cluFn7wTiGryunymYOu4RcffSxQluehd`


### Excercise 17
http://overthewire.org/wargames/bandit/bandit17.html

```bash
ssh bandit16@bandit.labs.overthewire.org -p 2220
cluFn7wTiGryunymYOu4RcffSxQluehd
```
