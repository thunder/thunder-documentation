
You can install extensions via the UI or the command line.

**UI**

You can install modules by going to your site page `admin/modules`, or by clicking on `Extend` in the menu at the top. Here you can search for the module already added to your project by entering the name in the filter box at the top. To actually install a module, select the checkbox next to it, scroll to the bottom and click `Install`. You might be warned that another module needs to be enabled because it is required for the module of your interest. By clicking on `continue`, Thunder will take care of that.

You can install themes by going to your site page `admin/appearance`, or by clicking on `Appearance` in the menu at the top. Here you can scroll to the theme you would like to install and click on `Install and set as default` to directly use the theme for your site.

**Command line**

To install a theme or module at the command line, you need to have [drush](http://docs.drush.org/en/master/install) installed.

You can run `drush` command in the `docroot` folder of your site to install a module like this:
```
$ drush en [module]
```

And to install a theme, you can run `drush` command like this:
```
$ drush then [theme]
```

To use a theme, you still have to navigate to `Appearance` (admin/appearance) and set it as default.
