# Configure Composer

* Install [Composer](https://getcomposer.org/)
* Create a `composer.json` file:

```
{
    "repositories": [
        {
            "type": "composer",
            "url": "http://packages.firegento.com"
        },
      {
        "type": "vcs",
        "url":  "git@github.com:opengento/codeception-magento-1.9.1.1.git"
      },
      {
        "type": "vcs",
        "url":  "git@github.com:opengento/codeception-magento.git"
      }
    ],
    "require": {
        "bragento/magento-composer-installer": "~1",
        "magento/core": "1.9.1.*",
        "colinmollenhour/modman": "*",
        "opengento/codeception-magento": "dev-master",
        "opengento/codeception-magento-1.9.1.1": "dev-master"
    },
    "scripts": {
        "modman": "vendor/bin/modman deploy-all --force"
    },
    "extra": {
        "magento-root-dir": "htdocs",
        "magento-force": 1,
        "magento-deploystrategy": "copy"
    }
}

```

* Install packages

```
composer install --no-dev
```
