# MageDawg Scouting4Magento

Sass Based Theme for Magento 2 Following Scouting Brand Guidelines V1.0 May 2018

## Installation

```BASH
composer config repositories.magedawg git git@github.com/MageDawg/magento2-theme-scouting4magento.git
composer require magedawg/theme-frontend-scouting4magento: "dev-master"
php bin/magento bin/magento setup:upgrade
```

## Compatibility

- Magento 2.2: v1.0.0 or later
- Magento 2.1: v0.11.0 or older
- Magento 2.0: v0.6.0 or older

## Bug Reports & Contribution Rules

- Before reporting an issue, check if you can reproduce it on the clean Magento instance with [SnowdogApps/magento2-theme-blank-sass](https://github.com/SnowdogApps/magento2-theme-blank-sass). If that's true, submit issue to the magento2-theme-blank-sass repository, not here
- If you know how to fix an issue, which is reproducible in Magento core, submit PR to the core product first, then here, with a link to PR in Magento 2 repository
- If issue is related only to the this theme, feel free to submit issue or PR


## Development

To develop this theme ensue you require dev modules with composer (default option)
This will install [SnowdogApps/magento2-frontools](https://github.com/SnowdogApps/magento2-frontools)
change directory to `magento/vendor/snowdog/frontools/`
and run `gulp tyles`
Setup your `themes.json` file like below
Make your modifications
then change directory to `magento/tools/`
and run `gulp styles` to compile css

### themes.json

```JSON
{
  "snowdog-blank-sass": {
    "src": "vendor/snowdog/theme-blank-sass",
    "dest": "pub/static/frontend/Snowdog/blank",
    "locale": ["en_GB"],
    "postcss": ["plugins.autoprefixer()"],
    "ignore": [".test"]
  },
  "scouting4magento": {
    "src": "app/design/frontend/MageDawg/scouting4magento",
    "dest": "pub/static/frontend/MageDawg/scouting4magento",
    "parent": "snowdog-blank-sass",
    "localeOverwrites": true,
    "postcss": ["plugins.autoprefixer()"],
    "locale": ["en_US"]
  }
}
```