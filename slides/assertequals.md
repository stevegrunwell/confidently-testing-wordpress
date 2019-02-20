### Equality

<dl>
    <dt class="fragment" data-fragment-index="0"><code>assertEquals()</code></dt>
    <dd class="fragment" data-fragment-index="0"><code>$expected == $actual</code>?</dd>
    <dd class="fragment" data-fragment-index="0"><pre class="hljs lang-php"><code>$this->assertEquals($expected, $actual);</code></pre></dd>
    <dt class="fragment" data-fragment-index="1"><code>assertSame()</code></dt>
    <dd class="fragment" data-fragment-index="1"><code>$expected === $actual</code>?</dd>
    <dd class="fragment" data-fragment-index="1"><pre class="hljs lang-php"><code>$this->assertSame($expected, $actual);</code></pre></dd>
</dl>

Note:

* Subtle difference, but assertSame() does strict comparisons
    - If comparing two objects, assertSame wants them to reference the same object
