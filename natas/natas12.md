# Level 11
http://overthewire.org/wargames/natas/natas12.html

```
Username: natas12
Password: EDXp0pS26wLKHZy1rDBPUZk0RKfLGIR3
URL:      http://natas12.natas.labs.overthewire.org
```

```php
function genRandomString() {
    $length = 10;
    $characters = "0123456789abcdefghijklmnopqrstuvwxyz";
    $string = "";    

    for ($p = 0; $p < $length; $p++) {
        $string .= $characters[mt_rand(0, strlen($characters)-1)];
    }

    return $string;
}

function makeRandomPath($dir, $ext) {
    do {
        $path = $dir."/".genRandomString().".".$ext;
    } while(file_exists($path));
    return $path;
}

function makeRandomPathFromFilename($dir, $fn) {
    $ext = pathinfo($fn, PATHINFO_EXTENSION);
    return makeRandomPath($dir, $ext);
}

if(array_key_exists("filename", $_POST)) {
    $target_path = makeRandomPathFromFilename("upload", $_POST["filename"]);

    if(filesize($_FILES['uploadedfile']['tmp_name']) > 1000) {
        echo "File is too big";
    } else {
        if(move_uploaded_file($_FILES['uploadedfile']['tmp_name'], $target_path)) {
            echo "The file <a href=\"$target_path\">$target_path</a> has been uploaded";
        } else{
            echo "There was an error uploading the file, please try again!";
        }
    }
} else {
?>
    <form enctype="multipart/form-data" action="index.php" method="POST">
        <input type="hidden" name="MAX_FILE_SIZE" value="1000" />
        <input type="hidden" name="filename" value="<? print genRandomString(); ?>.jpg" />
        Choose a JPEG to upload (max 1KB):<br/>
        <input name="uploadedfile" type="file" /><br />
        <input type="submit" value="Upload File" />
    </form>
<? } ?> 
```

**Ideas**

 * Attack randoim function? Insecure random?
 * Path traversal? Malicious filename?
 * Malicious file? Upload php file?

**Notes:**

 * No clear path to reveal password. Try to access it from `/etc/natas_webpass/natas13`
 * Php echo's `$targetPath` back to client. XSS / Server side scripting in filename?
 * Application clearly expects JPEG's but doesn't appear to really check or enforce this in any meaningful way.

**Flag:** ``
