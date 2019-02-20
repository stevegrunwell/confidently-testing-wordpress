### Testing Output

<pre class="fragment-replacement"><code class="hljs lang-php fragment fade-out" data-fragment-index="0">public function test_shortcode_output() {
    ob_start();
    do_shortcode( '[recent-posts title="Latest Posts"]' );
    $output = ob_get_clean();

    $this->assertContains( '&lt;h2&gt;Latest Posts&lt;/h2&gt;', $output );
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="0">public function test_shortcode_output() {
    $this->expectOutput( '&lt;h2&gt;Latest Posts&lt;/h2&gt;' );

    do_shortcode( '[recent-posts title="Latest Posts"]' );
}</code></pre>

Note:

Since a lot of template tags will echo content directly to the screen, it's important to be able to test output.

I prefer to use output buffering to capture the output in a string, then do checks on it.

If you know exactly what the output will look like, you can also use $this->expectOutput().
