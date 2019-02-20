### Testing assets

```php
public function test_styles_get_enqueued() {
    $this->assertFalse( wp_style_is( 'my-plugin-styles', 'enqueued' ) );

    do_action( 'enqueue_scripts' );

    $this->assertTrue( wp_style_is( 'my-plugin-styles', 'enqueued' ) );
}
```

Note:

The wp_script_is() and wp_style_is() functions are great for verifying the registration or enqueueing of scripts and styles, respectively.
