http://overthewire.org/wargames/bandit/


## Exercise 1
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

## Exercise 2
http://overthewire.org/wargames/bandit/bandit2.html

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

Flag: `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`

## Exercise 3
http://overthewire.org/wargames/bandit/bandit3.html
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```

Flag: `UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK`

## Exercise 4
http://overthewire.org/wargames/bandit/bandit4.html
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```

Flag: `pIwrPrtPN36QITSp3EQaw936yaFoFgAB`

## Exercise 5
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

## Exercise 6
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

## Exercise 7
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

## Exercise 8
http://overthewire.org/wargames/bandit/bandit8.html
```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```

```bash
grep "millionth" data.txt
millionth	cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```

## Exercise 9
http://overthewire.org/wargames/bandit/bandit9.html
```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```

```bash
cat data.txt | sort | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

## Exercise 10
http://overthewire.org/wargames/bandit/bandit9.html
```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

```bash
cat data.txt | strings | grep -E -a "=+"
```

## Exercise 11
http://overthewire.org/wargames/bandit/bandit10.html
```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```

```bash
cat data.txt | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPRcd
```


## Exercise 12
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

## Exercise 13
http://overthewire.org/wargames/bandit/bandit13.html
```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```

...

Flag: `8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL`

## Exercise 14
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

## Exercise 15
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

## Exercise 16
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


## Exercise 17

http://overthewire.org/wargames/bandit/bandit17.html

**Login**
```bash
ssh bandit16@bandit.labs.overthewire.org -p 2220
cluFn7wTiGryunymYOu4RcffSxQluehd
```

**Working**

```bash
nmap localhost -p31000-32000
```
```bash
Starting Nmap 7.40 ( https://nmap.org ) at 2019-08-05 04:11 CEST
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00019s latency).
Not shown: 999 closed ports
PORT      STATE SERVICE
31518/tcp open  unknown
31790/tcp open  unknown
```

```bash
nmap -sV localhost -p31518
```
```
Starting Nmap 7.40 ( https://nmap.org ) at 2019-08-05 04:22 CEST
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00011s latency).
PORT      STATE SERVICE  VERSION
31518/tcp open  ssl/echo

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 52.57 seconds
```

```bash
nmap -sV localhost -p31790
```
```
Starting Nmap 7.40 ( https://nmap.org ) at 2019-08-05 04:25 CEST
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00014s latency).
PORT      STATE SERVICE     VERSION
31790/tcp open  ssl/unknown
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port31790-TCP:V=7.40%T=SSL%I=7%D=8/5%Time=5D47939D%P=x86_64-pc-linux-gn
SF:u%r(GenericLines,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20cur
SF:rent\x20password\n")%r(GetRequest,31,"Wrong!\x20Please\x20enter\x20the\
SF:x20correct\x20current\x20password\n")%r(HTTPOptions,31,"Wrong!\x20Pleas
SF:e\x20enter\x20the\x20correct\x20current\x20password\n")%r(RTSPRequest,3
SF:1,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x20password\n
SF:")%r(Help,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x2
SF:0password\n")%r(SSLSessionReq,31,"Wrong!\x20Please\x20enter\x20the\x20c
SF:orrect\x20current\x20password\n")%r(TLSSessionReq,31,"Wrong!\x20Please\
SF:x20enter\x20the\x20correct\x20current\x20password\n")%r(Kerberos,31,"Wr
SF:ong!\x20Please\x20enter\x20the\x20correct\x20current\x20password\n")%r(
SF:FourOhFourRequest,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20cu
SF:rrent\x20password\n")%r(LPDString,31,"Wrong!\x20Please\x20enter\x20the\
SF:x20correct\x20current\x20password\n")%r(LDAPSearchReq,31,"Wrong!\x20Ple
SF:ase\x20enter\x20the\x20correct\x20current\x20password\n")%r(SIPOptions,
SF:31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x20password\
SF:n");

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 88.06 seconds
```

```bash
openssl s_client -connect localhost:31790
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
MIICBjCCAW+gAwIBAgIEIRCKRDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMTkwODAzMTU1MTQ5WhcNMjAwODAyMTU1MTQ5WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBALjLe4CV
y7o3TByY368V/nUFggs4EXLB6OPxbM7n9XR2fP5gBBFXeqT3jaupydtSYhWXTrgP
PqwB2Bk5v+v7twT6KZCM5ks54NgGqH8l48zzvqBFwvllQfpARfq0GTLixbrxuSmp
w9F8efzpOfxnoMdG9zvGBSm8M+UdAiQuprVpAgMBAAGjZTBjMBQGA1UdEQQNMAuC
CWxvY2FsaG9zdDBLBglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0
ZWQgYnkgTmNhdC4gU2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3
DQEBBQUAA4GBAHQ18wczrve2XIGz+hzhqZJ402L+pa5nl5ci76tTPtK0nAh4v+Ey
UlM+XvuL5l/opTiI6/+cObNUGOEpv8kVfwdAYiTr5RlXe9mBRErQl4r3PnhZylJM
cVD7/BsFM3uACmHVI5KRs2JSmnB4+sfZifHPxaMsLJvF6dUuHr+YC7E0
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
    Session-ID: 568EA7AA413AE5E7DC52619A15ABC1B0CD781C7B03617FCF0E2D9271E687CC0C
    Session-ID-ctx: 
    Master-Key: 7A3641570E7070D8FD61E1F684A04073608F7A9E7C2807F2B7BA212BA50BF1C40A335D3E32E4E8F78DBB238597074754
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 5c fe f6 48 80 2f 25 d8-f9 76 de 4d a7 c5 95 a7   \..H./%..v.M....
    0010 - 8d a1 ef ae 3b 30 f4 fb-70 82 f8 17 7f 68 3d 78   ....;0..p....h=x
    0020 - 81 0d b0 11 ac 99 27 5f-a9 a4 03 9a ea cd 67 eb   ......'_......g.
    0030 - 4b 4f ff b0 38 21 d3 87-61 81 fe ae 95 3d 72 46   KO..8!..a....=rF
    0040 - f2 c5 be 9b c7 0d 48 68-ac ad 95 ba e1 18 bf 89   ......Hh........
    0050 - 90 28 db ff 5c 77 3d df-bf c0 40 0b 07 89 37 ee   .(..\w=...@...7.
    0060 - 52 2e 8a 3f d4 b2 c1 cb-16 f4 8b 2d 35 48 bd a7   R..?.......-5H..
    0070 - ae 25 bd 49 09 f7 b8 6c-96 9e 2d 8e 31 16 e5 5a   .%.I...l..-.1..Z
    0080 - 05 b3 5d 5a bb 87 62 5e-b0 07 94 bb 71 2b f7 ab   ..]Z..b^....q+..
    0090 - e3 b9 96 2a 69 4c 57 aa-c5 c8 3f 3b e1 f2 62 de   ...*iLW...?;..b.

    Start Time: 1564972317
    Timeout   : 7200 (sec)
    Verify return code: 18 (self signed certificate)
    Extended master secret: yes
---
cluFn7wTiGryunymYOu4RcffSxQluehd
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
```

**Flag**:

```
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
```

## Exercise 18

http://overthewire.org/wargames/bandit/bandit18.html

**Login**

`bandit17.pem`
```
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
```

```bash
ssh -i ./bandit17.pem bandit17@bandit.labs.overthewire.org -p 2220
```

**Working**

```bash
diff passwords.old passwords.new
```
```
42c42
< hlbSBPAWJmL6WFDb06gpTx1pPButblOA
---
> kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
```

**Flag:** `kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd`

## Exercise 19

http://overthewire.org/wargames/bandit/bandit19.html

**Login**

```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220
kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
```

```
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password: 
Linux bandit 4.18.12 x86_64 GNU/Linux
               
      ,----..            ,----,          .---. 
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' ' 
  |   :  | ; | ' ;    |.';  ; ;   \  \;      : 
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ; 
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"  
     \   \ .'        ;   |.'       \   \ ;     
  www. `---` ver     '---' he       '---" ire.org     
               
              
Welcome to OverTheWire!

If you find any problems, please report them to Steven or morla on
irc.overthewire.org.

--[ Playing the games ]--

  This machine might hold several wargames. 
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ and /proc/ is disabled
  so that users can not snoop on eachother. Files and directories with 
  easily guessable or short names will be periodically deleted!

  Please play nice:
      
    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS! 
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro 

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few usefull tools which you can find
 in the following locations:

    * pwndbg (https://github.com/pwndbg/pwndbg) in /usr/local/pwndbg/
    * peda (https://github.com/longld/peda.git) in /usr/local/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /usr/local/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)
    * checksec.sh (http://www.trapkit.de/tools/checksec.html) in /usr/local/bin/checksec.sh

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us through IRC on
  irc.overthewire.org #wargames.

  Enjoy your stay!

Byebye !
Connection to bandit.labs.overthewire.org closed.
```

**Working**
```
ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat readme"
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5
```

**Flag:** `IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x`

## Exercise 20

http://overthewire.org/wargames/bandit/bandit20.html

**Login**

```bash
ssh bandit19@bandit.labs.overthewire.org -p 2220
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
```

**Working**

```bash
./bandit20-do cat /etc/bandit_pass/bandit20
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```

**Flag:** `GbKksEFF4yrVs6il55v6gwY5aVje5f0j`

## Exercise 21

http://overthewire.org/wargames/bandit/bandit21.html

**Login**

```bash
ssh bandit20@bandit.labs.overthewire.org -p 2220
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```

**Working**

```bash
echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l localhost -p 3333 &
```

```bash
./suconnect 3333
```

```
Read: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
Password matches, sending next password
gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
[3]-  Done                    echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l localhost -p 3333
```

**Flag**: `gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr`

## Exercise 22

http://overthewire.org/wargames/bandit/bandit22.html

**Login**

```bash
ssh bandit21@bandit.labs.overthewire.org -p 2220
gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
```

**Working**

```bash
ls -l /etc/cron.d
```
```
total 12
-rw-r--r-- 1 root root 120 Oct 16  2018 cronjob_bandit22
-rw-r--r-- 1 root root 122 Oct 16  2018 cronjob_bandit23
-rw-r--r-- 1 root root 120 Oct 16  2018 cronjob_bandit24
```
```bash
cat /etc/cron.d/cronjob_bandit22
```
```bash
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
```
```bash
cat /usr/bin/cronjob_bandit22.sh 
```
```
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```
```bash
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```
```
Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
```

**Flag:** `Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI`

## Exercise 23

http://overthewire.org/wargames/bandit/bandit23.html

**Login**

```bash
ssh bandit22@bandit.labs.overthewire.org -p 2220
Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
```

**Working**

```bash
cat /etc/cron.d/cronjob_bandit23
```
```
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
```

```bash
cat /usr/bin/cronjob_bandit23.sh
```
```bash
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user `bandit22` | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
```

```bash
cat /tmp/$(echo I am user bandit23 | md5sum | cut -d ' ' -f 1)
```
```
jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
```

**Flag:** `jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n`

## Exercise 24

http://overthewire.org/wargames/bandit/bandit24.html

**Login**

```bash
ssh bandit23@bandit.labs.overthewire.org -p 2220
jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
```

**Working**

```bash
cat /etc/cron.d/cronjob_bandit24.sh
```
```
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
```

```bash
cat /usr/bin/cronjob_bandit24.sh
```

```bash
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        timeout -s 9 60 ./$i
        rm -f ./$i
    fi
done
```

```bash
mkdir -m /tmp/me
```
```bash
cd /tmp/me
```
```bash
touch pwned.sh password
```
```bash
chmod -R 777 /tmp/me
```
```bash
nano password
```
```bash
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/me/password
```
```
cp pwned.sh /var/spool/bandit24/
```
```tail -f
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
```

**Flag:** `UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ`

## Exercise 25

http://overthewire.org/wargames/bandit/bandit25.html

**Login**

```
ssh bandit24@bandit.labs.overthewire.org -p 2220
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
```

```python
for i in range(10000):
    print("UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ {:04d}".format(i)) 
```

```bash
for i in {0:}
for i in range(10000):
    print("UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ {:04d}".format(i)) 
```

```bash
python3 pwned.py | nc localhost 30002 | sort | uniq
```

Correct!
Exiting.
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
The password of user bandit25 is uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG
Wrong! Please enter the correct pincode. Try again.
```

**Flag**: `uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG`