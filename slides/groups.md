### @group

Used to run tests of a similar nature, across suites & classes:

```php
/**
 * @group Posts
 * @group PostMeta
 */
public function test_includes_private_posts()
{
    // ...
}
```

```sh
$ phpunit --group=Posts
```
<!-- .element: class="fragment" -->

Note:

* The @group tag lets us group tests — no matter where they live — together
    - Really useful when different areas of the app need tested together
    - Completely user-defined, and test methods can belong to multiple groups
