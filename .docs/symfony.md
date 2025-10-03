# Symfony Documentation

## Installation

Example of installation instructions written in Markdown format, suitable for a README.md file. It includes steps for Composer installation and bundle enablement.

[Source](https://symfony.com/doc/4.x/bundles/best_practices)

```markdown
Installation
============

Make sure Composer is installed globally, as explained in the
[installation chapter](https://getcomposer.org/doc/00-intro.md)
of the Composer documentation.

Applications that use Symfony Flex
----------------------------------

Open a command console, enter your project directory and execute:

```console
$ composer require <package-name>
```

Applications that don't use Symfony Flex
----------------------------------------

### Step 1: Download the Bundle

Open a command console, enter your project directory and execute the
following command to download the latest stable version of this bundle:

```console
$ composer require <package-name>
```

### Step 2: Enable the Bundle

Then, enable the bundle by adding it to the list of registered bundles
in the `config/bundles.php` file of your project:

```php
// config/bundles.php

return [
    // ...
    <vendor>\<bundle-name>\<bundle-long-name>::class => ['all' => true],
];
```

## Setup Existing Symfony Project

Commands to set up an existing Symfony project, including cloning the repository and installing dependencies using Composer.

[Source](https://symfony.com/doc/7.3/setup)

```bash
# clone the project to download its contents
$ cd projects/
$ git clone ...

# make Composer install the project's dependencies into vendor/
$ cd my-project/
$ composer install
```
