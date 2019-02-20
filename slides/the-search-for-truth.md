### The search for truth

```php
// $this->assertEquals($expected, $actual);
$this->assertTrue($expected == $actual);
```
<!-- .element: class="fragment" -->

```php
// $this->assertNotContains($expected, $actual);
$this->assertFalse(in_array($expected, $actual));
```
<!-- .element: class="fragment" -->

```php
// $this->assertRegexp($regex, $actual);
$this->assertTrue((bool) preg_match($expected, $actual));
```
<!-- .element: class="fragment" -->

Note:

When we look at how these assertions work, we see that everything comes down to TRUE or FALSE
