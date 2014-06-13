# Slim PHP test

A Demo PHP Slim REST API app.

I got this running in about 10 minutes as a proof-of-concept / exploration of modern PHP.


## Tutorial

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

To launch the server:
`php -S localhost:3000`
