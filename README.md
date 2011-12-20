Readme
======

Install Dependencies:
---------------------
	$ sudo pear install channel://pear.php.net/Net_URL2-0.3.1
	$ sudo pear install channel://pear.php.net/HTTP_Request2-2.0.0RC1

Usage Example:
--------------
```php
<?php
	require_once('phpcclib.php');
	$api = new Api();
	$email = 'you@example.com';
	$password = '$3cr3t';
	$api->auth($email, $password);
?>
```