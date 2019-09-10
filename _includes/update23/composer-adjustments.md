We switched from bower-asset to npm-asset for our frontend-libraries.
In order to get the libraries downloaded to the correct location, please
replace
```
"installer-types": ["bower-asset"],
```
by
```
"installer-types": ["bower-asset", "npm-asset"],
```
in the composer.json of your project and add "type:npm-asset" to the "docroot/libraries/{$name}" section in installer-paths.


We moved the composer package under the thunder namespace, so remove the old package and a the new one.

```
composer remove burdamagazinorg/thunder
```

```
composer require "thunder/thunder-distribution:~3.3" --no-update
```

You have to update composer now.

```
composer update
```

We removed some modules from our codebase. In case you are using one of
below mentioned modules please require them manually for your project.

```
composer require drupal/views_load_more --no-update
composer require drupal/breakpoint_js_settings --no-update
composer require valiton/harbourmaster --no-update
composer require drupal/riddle_marketplace:~3.0 --no-update
composer require drupal/nexx_integration:~3.0 --no-update
composer require burdamagazinorg/infinite_module:~1.0 --no-update
composer require burdamagazinorg/infinite_theme:~1.0 --no-update
```
