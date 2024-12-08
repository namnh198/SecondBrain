---
title: Hyva Theme Magento
createDate: 2024-12-08
tags:
  - Web-Dev
  - Magento
---
## Installation

You need to buy and generate a license key and add Private Packagist to `composer.json`

```shell
composer config --auth http-basic.hyva-themes.repo.packagist.com token yourLicenseAuthentificationKey
composer config repositories.private-packagist composer https://hyva-themes.repo.packagist.com/yourProjectName/
```

Then, install the theme package and its dependencies

```shell
# install hyva-theme
composer require hyva-themes/magento2-default-theme

# setup magento
bin/magento setup:upgrade
bin/magento setup:di:complie
```

Switch current theme to `hyva/default` theme: `Content -> Design -> Configuration`
