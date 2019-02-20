### Checking for WP_Errors <!-- .element: class="wordpress-icon" -->

Was the response an instance of `WP_Error`?

```php
public function test_function_can_return_wp_error() {
    $response = myplugin_function();

    $this->assertWPError($response);
}
```

Note:

Since WordPress doesn't really use Exceptions, instead favoring the WP_Error class, the assertWPError() assertion included in the core test suite can be useful if you need to check for WP_Error instances.
