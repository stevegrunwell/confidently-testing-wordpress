### Testing permissions

```php
public function test_non_admins_cannot_clear_cache() {
    // Arrange
    $user_id = $this->factory->user->create( [
        'role' => 'author',
    ] );

    wp_set_current_user( $user_id );

    // Act
    $response = myplugin_clear_cache();

    // Assert
    $this->assertWPError($response);
    $this->assertSame(403, $response->get_error_code());
}
```

Note:

Imagine we have a function that clears the site cache, but the function should check the user's capabilities before doing anything. If the user doesn't have permission, we should get back a WP_Error object.

We'll start by arranging our test — creating a non-admin user and authenticating as them. Next, we'll call the myplugin_clear_cache() function (Act), then make assertions against the response. Is it a WP_Error, and are we getting the error code we expect?
