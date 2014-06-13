# Slim PHP test

A Demo PHP Slim REST API app.

I got this running in about 10 minutes as a proof-of-concept / exploration of modern PHP.

## Package Management

- Composer
  https://getcomposer.org

## REST API Framework

- Slim 
  http://www.slimframework.com

## Tutorial
In terminal:
```
brew install php55
brew install composer
vim composer.json
```

`composer.json`

```json
{
  "require": {
    "slim/slim": "2.*"
  }
}
```
Again in terminal:
```
composer install
vim index.php
```

`index.php`

```php
<?php

require 'vendor/autoload.php';

$app = new \Slim\Slim();

$app->get('/:name', function ($name) {
  echo "Hello, $name";
});

$app->run();

?>
```

To launch the server, from terminal:
`php -S localhost:3000`
