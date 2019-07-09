# Extending Thunder

### Find an extension

You can find extensions on [Drupal.org](https://www.drupal.org). On [the following page](https://www.drupal.org/project/project_module?f%5B3%5D=drupal_core%3A7234), you can search for `Modules` and on [this page](https://www.drupal.org/project/project_theme?f%5B2%5D=drupal_core%3A7234) for `Themes`. You can find extensive documentation on [Drupal 8 User Guide - Extending and Customizing Your Site](https://www.drupal.org/docs/user_guide/en/extend-chapter.html).

If you know what extension you want, the fastest way is to google it, adding `drupal` to the search. For example: `drupal webform`

### Add an extension to your project

With `composer`, you can manage also the dependencies of your Thunder site and extensions.

To add an extension to your project, go to the root of your site (there should be a `composer.json` file) and add modules by typing
```
$ composer require drupal/[shortname of the extension]
```
into the command line.

For example:

```
$ composer require drupal/webform
```

### Install an extension

You can install extensions via the UI or the command line.

**UI**

You can install modules by going to your site page `/admin/modules`, or by clicking on `Extend` in the menu at the top. Here you can search for the module, by entering the name in the filter box at the top. To actually install a module, select the checkbox next to it, scroll to the bottom and click `Install`. You might be warned that another module needs to be enabled because it is required for the module of your interest. By clicking on `continue`, Thunder will take care of that.

You can install themes by going to your site page `/admin/appearance`, or by clicking on `Appearance` in the menu at the top. Here you can scroll to the theme, you would like to install and click on `Install` to install it, or click on `Install and set as default` to use the theme for your site, after installing it.

**Command line**

To install a theme or module at the command line, you need to have [drush](http://docs.drush.org/en/master/install) installed.

You can run `drush` command in the `docroot` folder of your site to install a module or theme like this:
```
$ drush en [extension]
```

To use a theme, you still have to either set it as default.
