### [PHPUnit Markup Assertions](https://github.com/stevegrunwell/phpunit-markup-assertions)

Assertions powered by DOMDocument:

```php
function test_button_contains_active_state() {
    $output = some_function();

    $this->assertContainsSelector('.button.active', $output);
}
```

Note:

A bit of self-promotion, but sometimes you need to test that a certain ID is present or a specific element contains text.

This PHPUnit Markup Assertions library has a set of assertions that wrap around PHP's DOMDocument.
