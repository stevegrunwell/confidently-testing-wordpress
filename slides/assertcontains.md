### Verifying contents

<dl>
    <dt class="fragment" data-fragment-index="0"><code>assertContains()</code></dt>
    <dd class="fragment" data-fragment-index="0">Does <code>$value</code> contain <code>$expected</code>?</dd>
    <dd class="fragment" data-fragment-index="0"><pre class="hljs lang-php"><code>$this->assertContains('bar', 'Foo bar baz');</code></pre></dd>
    <dd class="fragment" data-fragment-index="1"><pre class="hljs lang-php" style="margin-top: 0;"><code>$this->assertContains('b', ['a', 'b', 'c']);</code></pre></dd>
    <dt class="fragment" data-fragment-index="2"><code>assertRegexp()</code></dt>
    <dd class="fragment" data-fragment-index="2">Does <code>$value</code> match the given <code>$regex</code>?</dd>
    <dd class="fragment" data-fragment-index="2"><pre class="hljs lang-php"><code>$this->assertRegexp('/^Fo+/', 'Foo Bar');</code></pre></dd>
</dl>

Note:

* Types matter!
    - assertContains() will look for sub-strings if given a string, or values if given an array
