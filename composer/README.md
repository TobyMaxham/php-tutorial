# Composer

-----

Everything you should know about the [Dependency Management for PHP](https://github.com/composer/composer)

-----

## Installation / Usage

```sh
$ curl -sS https://getcomposer.org/installer | php
$ sudo mv composer.phar /usr/local/bin/composer
```

Alternatively you can use the executable [`composer.phar`](https://getcomposer.org/composer.phar).

```sh
$ composer require tobymaxham/url-shortener
```
... will create a `composer.json` file ...
```json
{
    "require": {
        "tobymaxham/url-shortener": "^1.1"
    }
}
```
... also all required dependencies will be installed under `/vendor/`.