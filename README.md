Readme
======

Install With Composer:
----------------------
Get composer to your project folder:
~~~bash
$ curl -s https://getcomposer.org/installer | php
~~~

Create a file `composer.json` with:
~~~
{
    "require": {
        "cloudcontrol/phpcclib": "dev-master"
    },
    "repositories": [
        {
            "type": "pear",
            "url": "http://pear.php.net"
        }
    ]
}
~~~

Run in your project folder:
~~~bash
$ ./composer.phar install
~~~

Usage Example:
--------------
~~~php
<?php
require 'vendor/autoload.php';
use CloudControl\API;

$api = new Api();
$email = 'mw@cloudcontrol.de';
$password = 'yeah1834';
$api->auth($email, $password);

foreach($api->application_getList() as $app){
    printf("%s (%s)%s", $app->name, $app->type->name, PHP_EOL);
}
?>
~~~
