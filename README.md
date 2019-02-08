Lerna Test Consumer Project
===========================

This repo is a test to see if we can consume npm packages as composer packages… It can.

Notes:

* npm packages are installed that contain a `composer.json` and php files (as well as other assets)
* the `wikimedia/composer-merge-plugin` composer package looks for `composer.json` files in `./node_modules/@newism/*/composer.json` (blob)
* when a package is installed from npm running `composer update --lock` which will find all the new composer packages and update them
* if `wikimedia/composer-merge-plugin` finds any `composer.json` files they are merged into the projects `composer.json` file and downloaded (including dependencies) from packagist.

The lerna mono repo can be found here: https://github.com/newism/lerna