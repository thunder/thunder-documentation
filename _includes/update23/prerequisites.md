These are the instructions to manually update your existing Thunder 2 installation to Thunder 3. If you want to do a fresh installation of thunder please visit [install Thunder](https://thunder.github.io/thunder-documentation/quick-install) The most
significant change is the migration to media in core. But we also made
some changes to our composer.json.

You have to make sure, that your Thunder 2 project and all it's dependecies,
are fully updated to the most current versions. Run the following command in your docroot:

```
drush ev "print drupal_get_installed_schema_version('thunder') . PHP_EOL;"
```
This should print the number 8138 or greater. If that is not the case, update your project.

```
cd ..
composer update
```
This should update to Thunder 8.2.47 or greater.

Now run database updates:
```
cd docroot
drush updb
```
You should at least see the thunder 8138 schema update. If not, double check that the correct version of Thunder is installed, and that `drush updb` did not throw any errors.
