### What do we get?

* <!-- .element: class="fragment" --> `phpunit.xml.dist`
* <!-- .element: class="fragment" --> `.phpcs.xml.dist`
* <!-- .element: class="fragment" --> `.travis.yml`
* <!-- .element: class="fragment" --> `bin/install-wp-tests.sh`
* <!-- .element: class="fragment" --> `tests/bootstrap.php`
* <!-- .element: class="fragment" --> `tests/test-sample.php`

Note:

* phpunit.xml.dist is our PHPUnit configuration
* PHP_CodeSniffer configuration, ready for WordPress coding standards
* .travis.yml is the Travis CI config. WP-CLI can also generate files for other popular CI providers
* install-wp-tests.sh will create a local instance of WordPress to test with
    * Tools like VVV will already ship with a test environment
* bootstrap.php loads the WordPress tests into the test runner (more in a sec)
* test-sample.php is an example test
