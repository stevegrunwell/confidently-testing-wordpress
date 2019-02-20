### `markTestIncomplete()`<br>`markTestSkipped()`

<pre><output class="hljs">PHPUnit 7.1.5 by Sebastian Bergmann and contributors.

...<span class="text-notice">S</span>..<span class="text-notice">I</span>.....                           12 / 12 (100%)

Time: 1.14 seconds, Memory: 2.00MB

<span class="highlight-warning">OK, but incomplete, skipped, or risky tests!
Tests: 12, Assertions: 14, Skipped: 1, Incomplete 1.</span></output></pre>

Note:

* markTestIncomplete() = test hasn't yet been finished
    - Great for scaffolding out tests to be filled in
* markTestSkipped() = test should be skipped
    - Could be interfering with test suite
    - Best used for debugging, can be a red flag otherwise!
