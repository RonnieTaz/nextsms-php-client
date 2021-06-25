# Getting started

## Installation

```sh
composer require nextsms/php-client
```


## Usage



```php
require 'vendor/autoload.php';

use NextSMS\SDK\Client;

// Intiate with credentials
$client = new Client([
    'username' => 'YOUR_USERNAME',
    'password' => 'YOUR_PASSWORD',
    'enviroment' => 'testing', // or production
]);

// Setup the transaction
$data = [
    'from'  => 'NEXTSMS',
    'to'    => '2557123456789',
    'text'  => 'Hello World',
];

// Execute
$result = $client->singleDestination($data);

// Print results
var_dump($result);
```
