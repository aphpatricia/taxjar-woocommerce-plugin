# TaxJar Unit Tests

## Initial Setup

1) Install [PHPUnit](http://phpunit.de/) by following their [installation guide](https://phpunit.de/getting-started.html). If you've installed it correctly, this should display the version:

    $ phpunit --version

2) Install WordPress and the WP Unit Test lib using the `install.sh` script. Change to the plugin root directory and type:

    $ tests/bin/install.sh <db-name> <db-user> <db-password> [db-host]

**Important**: The `<db-name>` database will be created if it doesn't exist and all data will be removed during testing.

Sample usage:

    $ tests/bin/install.sh taxjar_tests root root

3) Set your TaxJar API key as a environment variable with the key of TAXJAR_API_TOKEN.

    $ export TAXJAR_API_TOKEN='123456789abcdef'

4) Make sure you have the WooCommerce plugin downloaded to your plugins directory.

## Running Tests

Go to the `/tests` directory in the command line and type:

    $ phpunit

You can run specific tests by providing the path and filename to the test class:

    $ phpunit specs/test-actions.php
