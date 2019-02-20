### Testing hooks

```php
public function test_function_does_action() {
    $called = false;

    // Register a callback to validate arguments.
    add_action( 'myplugin_action', function () use (&$called) {

        // Only return true if validations passed.
        $called = true;
    } );

    myplugin_function();

    $this->assertTrue( $called );
}
```

Note:

If you need to validate the arguments passed to the hook, you might register a callback on the hook being tested, letting you do anything you might need to do.

Notice that the $called variable is being passed by reference!
