# Install Thunder

### System requirements

You have to install `php`, `composer` and `git` on your computer in oder to install Thunder. The `composer` requires `git` command for proper functioning.

To install `php` please take a look at official [Installation and Configuration](https://www.php.net/manual/install.php) for `php`.
On top of `php` you need to install required libraries. Thunder installation requires following `php` libraries: `xmlwriter`, `gd`, `mbstring`, `curl`, `json` and `pdo_sqlite`. The installation of `php` extensions can defer between operating system, that's why you should check for detailed instructions on `php` [Installation and Configuration](https://www.php.net/manual/install.php) page.

To install `composer`, you can check [installation instructions](https://getcomposer.org/download) and for `git` you can find installation instructions [here](https://git-scm.com/downloads).

### Quick start installation
To start quickly, run this in your terminal to install Thunder from command line:

```
composer create-project thunder/thunder-project thunder --no-interaction --no-install
cd thunder
composer install
composer drupal:scaffold
cd docroot
php core/scripts/drupal quick-start thunder
```

### Beyond the quick start installation

For any further information please refer to [Drupal 8 User Guide](https://www.drupal.org/docs/user_guide/en/index.html).
