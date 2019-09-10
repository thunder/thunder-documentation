To uninstall an extension, you have to uninstall it first and then remove the code. You can uninstall extensions via the UI or the command line, but to remove the code from your project, you have to use `composer`.

**Uninstall in UI**

You can uninstall modules by going to your site page `admin/modules`, or by clicking on `Extend` in the menu at the top and then by clicking on `Uninstall` tab. Here you can search for the module by entering the name in the filter box at the top. To uninstall a module, select the checkbox next to it, scroll to the bottom and click `Uninstall`. You might be warned that another module needs to be uninstalled because it depends on the module that you want to remove. By clicking on `continue`, Thunder will take care of that.

You can uninstall themes by going to your site page `admin/appearance`, or by clicking on `Appearance` in the menu at the top. Here you can scroll to the theme you would like to uninstall. If your site is using that theme as default, you have to select another default theme before you can uninstall it. When your site is not using that theme as default, you can click `Uninstall` next to it to uninstall it.

**Uninstall with command line**

To uninstall a theme or module at the command line, you need to have [drush](http://docs.drush.org/en/master/install) installed.

After that, you can run `drush` command in the `docroot` folder of your site to uninstall a module like this:

```
$ drush pm:uninstall [module]
```

To uninstall a theme, you still have to select another theme as default. It's explained in `Uninstall in UI` part.

And then you to uninstall a theme, you can run `drush` command like this:
```
$ drush theme:uninstall [theme]
```
