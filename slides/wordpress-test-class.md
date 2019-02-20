### Base Test Class

<pre class="fragment-replacement"><code class="hljs lang-php fragment fade-out" data-fragment-index="0"># Standard PHPUnit
class MyAppTest extends PHPUnit\Framework\TestCase {
    // Include test methods.
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="0"># WP core test suite
class MyAppTest extends WP_UnitTestCase {
    // Include test methods for WordPress.
}</code></pre>

Note:

* If we were just using PHPUnit by itself, we'd extend PHPUnit\Framework\TestCase
* For WordPress, extend the core test suite: WP_UnitTestCase
    - Handles bootstrapping of WordPress along with resets between tests
