First we should make sure that the latest drush version is installed.
```
composer require drush/drush:~9.7.0 --no-update
```

After that the following steps should be done for the update:

```
composer require drupal/media_entity:^2.0 drupal/media_entity_image drupal/video_embed_field:^2.2
```

* Make sure that you use the "Media in core" branch for all your
media_* modules. (For the media modules in Thunder, we take care of that)
* Make sure that all your code that uses media_entity API is modified to use the core media API.

See here for more information:
* [Moved a refined version of the contributed Media entity module to core as Media module](https://www.drupal.org/node/2863992)
* [FAQ - Transition from Media Entity to Media in core](https://www.drupal.org/docs/8/core/modules/media/faq-transition-from-media-entity-to-media-in-core#upgrade-instructions-from-media-entity-contrib-to-media-in-core)
