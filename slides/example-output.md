<pre class="fragment-replacement"><output class="hljs fragment fade-out" data-fragment-index="0" style="max-height: none;">PHPUnit 7.5.1 by Sebastian Bergmann and contributors.

...............................................  47 / 511 (  9%)
...............................................  94 / 511 ( 18%)
...................................<span class="text-notice">SSSS</span>........ 141 / 511 ( 27%)
............................................... 188 / 511 ( 36%)
............................................... 235 / 511 ( 45%)
............................................... 282 / 511 ( 55%)
............................................... 329 / 511 ( 64%)
............................................... 376 / 511 ( 73%)
............................................... 423 / 511 ( 82%)
............................................... 470 / 511 ( 91%)
.........................................       511 / 511 (100%)

Time: 1.13 minutes, Memory: 42.00MB

<span class="highlight-warning">OK, but incomplete, skipped, or risky tests!
Tests: 511, Assertions: 1085, Skipped: 4.</span></output><output class="hljs fragment fade-in" data-fragment-index="0" style="max-height: none;">PHPUnit 7.5.1 by Sebastian Bergmann and contributors.

.......<span class="highlight-fail">F</span>........                                 16/16 (100%)

Time: 7.15 seconds, Memory: 14.00MB

There was 1 failure:

1) Tests\CoffeeTest::test_get_good_coffee
Failed asserting that two strings are identical.
--- Expected
+++ Actual
@@ @@
-'great, well-balanced coffee'
+'Starbucks'

/my-plugin/tests/test-coffee.php:14

<span class="highlight-fail">FAILURES!</span>
<span class="highlight-fail">Tests: 16, Assertions: 19, Failures: 1.</span></output></pre>

Note:

* When we chain all of our tests together, we get something that looks like this
* Example output from actual app
    - Four skipped tests, but everything passes
* Failures will show up in red, telling us what assertion(s) failed
