These are the instructions to manually update your existing Thunder 3 installation to Thunder 6 including Drupal 9. If you want to do a fresh installation of thunder please visit [install Thunder](https://thunder.github.io/thunder-documentation/quick-install).

**The most important change is that we removed the support for AMP and Facebook Instant Articles, because none of them support Drupal 9 currently. If you rely on one of these modules, we recommend that you stay on Thunder 3.5 for now.**

You have to make sure that your Thunder 3 project and all its dependencies
are fully updated to the most current versions. Run the following command in your docroot:

```
drush ev "print drupal_get_installed_schema_version('thunder') . PHP_EOL;"
```
This should print the number 8309 or greater. If that is not the case, update your project.

```
cd ..
composer update
```
This should update to Thunder 8.3.5 or greater.

Now run database updates:
```
cd docroot
drush updb
```
You should at least see the Thunder 8308 schema update. If not, double check that the correct version of Thunder is installed, and that `drush updb` did not throw any errors.

Before you start with the code and database update please disable the libraries module. The libraries module is not Drupal 9 compatible and
its most used functionality is now part of Drupal core. It is therefore not needed anymore. If you use other contrib modules that require the libraries module, please check if these modules support the new core functionality.
See [https://www.drupal.org/node/3099614](https://www.drupal.org/node/3099614)
