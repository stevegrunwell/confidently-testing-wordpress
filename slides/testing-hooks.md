### Testing hooks

```php
public function test_function_does_action() {
    myplugin_function();

    $this->assertSame( 1, did_action( 'myplugin_action' ) );
}
```

Note:

If we want to make sure that a custom action was called, we can use did_action() to see how many times it was called.

In this case, did myplugin_function() call do_action() on the myplugin_action hook?
