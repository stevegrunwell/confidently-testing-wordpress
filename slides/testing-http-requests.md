### Mocking HTTP Requests

```php
add_filter( 'pre_http_request', function () {
    return [
        'headers'  => [],
        'body'     => '',
        'response' => [
            'code'    => 200,
            'message' => 'OK',
        ],
        'cookies'  => [],
        'filename' => '',
    ];
} );
```

Note:

The pre_http_request filter will let us short-circuit responses from the WordPress HTTP API.

By stubbing responses from external APIs, our tests won't have to rely on these external APIs. Remember the System Under Test: we're not testing the API, we're testing how we interact with it.
