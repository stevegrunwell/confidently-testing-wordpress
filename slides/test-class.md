### Test Classes

<pre class="fragment-replacement"><code class="hljs lang-php fragment fade-out" data-fragment-index="0">class MyAppTest extends PHPUnit\Framework\TestCase
{
    // Include test methods.
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="0">class MyTestClass extends PHPUnit\Framework\TestCase {
    // Common functionality.
}

class MyAppTest extends MyTestClass
{
    // Include test methods.
}</code></pre>

Note:

* A test class typically extends the PHPUnit\Framework\TestCase class
* If you have functionality common between classes, consider creating your own base test class
    - Could also be moved into PHP traits
