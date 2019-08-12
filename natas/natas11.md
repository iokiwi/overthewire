# Level 11
http://overthewire.org/wargames/natas/natas11.html

```
Username: natas11
Password: U82q5TCMMQ9xuFoI3dYX61s7OZD9JKoK
URL:      http://natas11.natas.labs.overthewire.org
```

```php
<?


function xor_encrypt($in) {
    $key = '<censored>';
    $text = $in;
    $outText = '';
    // Iterate through each character
    for($i=0; $i < strlen($text); $i++) {
        $outText .= $text[$i] ^ $key[$i % strlen($key)];
    }
    return $outText;
}

function loadData($def) {
    global $_COOKIE;      
    $mydata = $def;
    if(array_key_exists("data", $_COOKIE)) {
        $tempdata = json_decode(xor_encrypt(base64_decode($_COOKIE["data"])), true);
        if(is_array($tempdata) && array_key_exists("showpassword", $tempdata) && array_key_exists("bgcolor", $tempdata)) {
            if (preg_match('/^#(?:[a-f\d]{6})$/i', $tempdata['bgcolor'])) {
                $mydata['showpassword'] = $tempdata['showpassword'];
                $mydata['bgcolor'] = $tempdata['bgcolor'];
            }
        }
    }
    return $mydata;
}

function saveData($d) {
    setcookie("data", base64_encode(xor_encrypt(json_encode($d))));
}

$defaultdata = array( "showpassword"=>"no", "bgcolor"=>"#ffffff");

$data = loadData($defaultdata);

if(array_key_exists("bgcolor",$_REQUEST)) {
    if (preg_match('/^#(?:[a-f\d]{6})$/i', $_REQUEST['bgcolor'])) {
        $data['bgcolor'] = $_REQUEST['bgcolor'];
    }
}

saveData($data);

?>

<h1>natas11</h1>
<div id="content">
<body style="background: <?=$data['bgcolor']?>;">
Cookies are protected with XOR encryption<br/><br/>

<?
if($data["showpassword"] == "yes") {
    print "The password for natas12 is <censored><br>";
}
?>

<form>
Background color: <input name=bgcolor value="<?=$data['bgcolor']?>">
<input type=submit value="Set color">
</form>
```

```php

$a = json_encode(array( "showpassword"=>"no", "bgcolor"=>"#ffffff"));
$b = base64_decode("ClVLIh4ASCsCBE8lAxMacFMZV2hdVVotEhhUJQNVAmhSMX4MNzF+aAw=");

for($i = 0; $i < strlen($a); $i++){
    echo $a[$i] ^ $b[$i];
}

// qw8Jqw8Jqw8Jqw8Jqw8Jqw8Jqw8J...
```

So `$key` = `qw8J`

```php
function xor_encrypt($in) {
    $key = 'qw8J';
    $text = $in;
    $outText = '';
    for($i=0; $i < strlen($text); $i++) {
        $outText .= $text[$i] ^ $key[$i % strlen($key)];
    }
    return $outText;
}

$a = array( "showpassword"=>"yes", "bgcolor"=>"#ffffff");
$b = base64_encode(xor_encrypt(json_encode($a)));
var_dump($b); 
// ClVLIh4ASCsCBE8lAxMacFMOXTlTWxooFhRXJh4FGnBTVF4sFxFeLFMK=
```

Then set cookie to new encrypted value and resend with bgcolor = #ffffff

**Flag:** `The password for natas12 is EDXp0pS26wLKHZy1rDBPUZk0RKfLGIR3`
