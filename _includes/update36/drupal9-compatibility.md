Because Thunder 6 is based on Drupal 9, check your compatibility before your run the upgrade.

Drupal.org provides a good documentation for that: [https://www.drupal.org/docs/upgrading-drupal/how-to-prepare-your-drupal-7-or-8-site-for-drupal-9](https://www.drupal.org/docs/upgrading-drupal/how-to-prepare-your-drupal-7-or-8-site-for-drupal-9)


### Check compatibility by running tests

If your test suite is based on Drupal tests, eg Functional oder FunctionalJavascript, you can configure your tests to fail
when calling deprecated code.

Add the following line to your phpunit.xml file and run your tests.

```
    <env name="SYMFONY_DEPRECATIONS_HELPER" value="strict"/>
```
