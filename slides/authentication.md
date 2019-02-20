### Impersonating users <!-- .element: class="wordpress-icon" -->

Act as users with different roles & capabilities:

```php
public function test_authors_cant_blow_stuff_up() {
    $user_id = $this->factory->user->create( [
        'role' => 'author',
    ] );

    wp_set_current_user( $user_id );

    $this->assertFalse( current_user_can( 'blow_stuff_up' ) );
}
```

Note:

If you need to do any sort of permission checks, you'll likely find yourself doing this: create a new user, then use wp_set_current_user() to tell WordPress you're acting as the given user ID.
