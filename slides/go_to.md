### go_to() <!-- .element: class="wordpress-icon" -->

Change the current page context:

```php
public function test_go_to_usage() {
    $this->assertFalse( is_home() );

    $this->go_to( '/blog' );

    $this->assertTrue( is_home() );
}
```

Note:

Lets you change the current page context, but does not actually load a page. Works by resetting the current page query.

Sets super globals, globals, query variables, main query as if the given page was requested.
