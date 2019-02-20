### Test method

<pre class="fragment-replacement"><code class="hljs lang-php fragment fade-out" data-fragment-index="0">public function test_it_does_something()
{
    // Arrange, act, then assert.
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="0">/**
 * @test
 */
public function it_should_do_something()
{
    // Arrange, act, then assert.
}</code></pre>

Note:

* Test methods are public methods declared within the test class
* By convention, methods begin with "test"
    - Some people prefer to write more descriptive test names
    - Can use @test DocBlock tag instead
