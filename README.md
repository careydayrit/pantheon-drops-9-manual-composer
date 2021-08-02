# Drupal 9 Manual Composer for Pantheon

Note:
This comes with no guarante this repo is for educational purposes only not an official Pantheon repo

Use the following direct link to create a new site on Pantheon:

https://dashboard.pantheon.io/sites/create?upstream_id=76da4192-1d0f-480b-b8f4-accbeeae458e


Avoid confusion by moving your site to an empty upstream:
```
terminus site:upstream:set <sitename> empty
```

Ongoing Core Updates

```
composer update drupal/core --with-dependencies
composer prepare-for-pantheon
composer install --no-dev
```

Working with Lando


`lando init --source=pantheon`

Edit .lando.yml and add the line at the bottom.  Chane the framework to drupal 9

```
config:
  framework: drupal9

services:
  database:
    type: mariadb:10.4
```

Issue lando rebuild, start then pull 

```
lando rebuild
lando start
lando pull
lando drush cr
```


