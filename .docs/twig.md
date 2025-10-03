# Twig Documentation

## Installation

The recommended way to install Twig is via Composer. This command adds the Twig library as a dependency to your project, ensuring you get the latest stable version compatible with your PHP environment.

[Source](https://twig.symfony.com/doc/3.x/intro)

```shell
composer require "twig/twig:^3.0"
```

## Basic Usage

This PHP snippet demonstrates how to set up a basic Twig environment. It includes requiring the autoloader, instantiating a `FilesystemLoader` to specify the template directory, and creating a `\Twig\Environment` instance with a compilation cache path. This setup is crucial for loading and compiling Twig templates efficiently.

[Source](https://twig.symfony.com/doc/3.x/api)

```php
require_once '/path/to/vendor/autoload.php';

$loader = new \Twig\Loader\FilesystemLoader('/path/to/templates');
$twig = new \Twig\Environment($loader, [
    'cache' => '/path/to/compilation_cache',
]);
```

This example demonstrates basic Twig API usage by loading a template directly from an array. It initializes a Twig environment with an ArrayLoader and renders a simple template, passing a variable for output.

[Source](https://twig.symfony.com/doc/3.x/intro)

```php
require_once '/path/to/vendor/autoload.php';

$loader = new \Twig\Loader\ArrayLoader([
    'index' => 'Hello {{ name }}!',
]);
$twig = new \Twig\Environment($loader);

echo $twig->render('index', ['name' => 'Fabien']);
```
