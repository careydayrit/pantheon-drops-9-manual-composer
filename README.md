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

