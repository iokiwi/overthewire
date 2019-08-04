### Excercise 0

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
bandit0
```

### Excercise 1

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

### Excercise 2

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```

### Excercise 3

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```

### Excercise 4

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

### Excercise 5

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```

```bash
ls -laR inhere | grep 1033 -C10
cat inhere/maybehere07/.file2
```

### Excercise 6

```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```

```bash
find / -user bandit7 -group bandit6
cat /var/lib/dpkg/info/bandit7.password
```

### Excercise 7

```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```

```bash
grep "millionth" data.txt
millionth	cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```

### Excercise 8

```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```

```bash
cat data.txt | sort | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

### Excercise 9

```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

```bash
cat data.txt | strings | grep -E -a "=+"
```

### Excercise 10

```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```

```bash
cat data.txt | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPRcd
```

### Excercise 11

```bash
ssh bandit11@bandit.labs.overthewire.org -p 2220
IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```

### Excercise 12

```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```

### Excercise 13

```bash
ssh bandit13@bandit.labs.overthewire.org -p 2220
8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```

### Excercise 14

```bash
ssh bandit14@bandit.labs.overthewire.org -p 2220
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
```

### Excercise 15

```bash
ssh bandit14@bandit.labs.overthewire.org -p 2220
BfMYroe26WYalil77FoDi9qh59eK5xNr
```

### Excercise 16

```bash
ssh bandit14@bandit.labs.overthewire.org -p 2220
cluFn7wTiGryunymYOu4RcffSxQluehd
```