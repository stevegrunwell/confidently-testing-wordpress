### Bootstrap File

<pre class="hljs"><code class="hljs lang-php">// 1. Locate the WordPress installation
$_tests_dir = getenv( 'WP_TESTS_DIR' );
if ( ! $_tests_dir ) {
    $_tests_dir = '/tmp/wordpress-tests-lib';
}</code><code class="hljs lang-php fragment" data-fragment-index="0">
// 2. Gain access to the tests_add_filter() function.
require_once $_tests_dir . '/includes/functions.php';</code><code class="hljs lang-php fragment" data-fragment-index="1">
// 3. Load the main plugin file.
tests_add_filter( 'muplugins_loaded', function () {
    require dirname( dirname( __FILE__ ) ) . '/my-plugin.php';
} );</code><code class="hljs lang-php fragment" data-fragment-index="2">
// 4. Bootstrap WordPress core.
require $_tests_dir . '/includes/bootstrap.php';</code></pre>

Note:

Basic outline of the bootstrap file, adjust for your needs:

1. Locate the test directory, which would be installed by the install-wp-tests shell script
2. Load in a file from the test environment so we have access to the tests_add_filter() function
3. Register a callback that explicitly loads your main plugin file
4. Load the core test suite's bootstrap file
