After you have uninstalled an extension from your site, you can also remove the code from your project.

If you want to remove a module, that was provided by Thunder, you will have to add it to your composer.json file in the
 replace block. Modules, that you added yourself by the above commands, do not have to be placed there.

```
 "replace": {
     "drupal/google_analytics": "*"
 }
```

For more information on using the composer replace check the official [composer documentation](https://getcomposer.org/doc/04-schema.md#replace)

To remove code you can execute a command like this:

```
$ composer remove drupal/[short name of the extension]
```
