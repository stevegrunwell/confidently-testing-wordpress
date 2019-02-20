### What don't we get?

```sh
$ composer init
```

```json
{
    "name": "stevegrunwell/test-plugin",
    "description": "An example WordPress plugin WITH TESTS!",
    "type": "wordpress-plugin",
    "license": "MIT",
    "authors": [
        {
            "name": "Steve Grunwell",
            "homepage": "https://stevegrunwell.com"
        }
    ],
    "require-dev": {
        "phpunit/phpunit": "^7.0"
    }
}
```
<!-- .element: class="fragment" -->

Note:

* It's worth noting that WP-CLI will not generate a composer.json file for us
* Some people like to rely on global PHPUnit installations, but this ensures that all developers and environments use the same version of PHPUnit
    * Also worth noting that the core test suite does not yet support PHPUnit 8.
