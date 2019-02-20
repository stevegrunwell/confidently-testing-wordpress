### Registering a custom post type

```php
public function test_book_cpt_is_registered() {
    myplugin_register_post_types();

    $post_type = get_post_type_object( 'book' );

    // Verify the post type is registered along with key properties.
    $this->assertNotNull( $post_type );
    $this->assertTrue( $post_type->public );
    $this->assertFalse( $post_type->hierarchical );
}
```

Note:

A common test might be ensuring that a custom post type is being registered.

Isn't much of an arrange step, but we're going to call our function (ACT), then inspect the registered post type. We don't need to check everything, but make sure the important properties are set as we expect.
