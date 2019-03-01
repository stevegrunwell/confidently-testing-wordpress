### Regression tests

```php
/**
 * @test
 * @testWith [0, "There have been no posts in the last 30 days."]
 *           [1, "One post in the last 30 days."]
 *           [2, "2 posts in the last 30 days."]
 */
public function recent_posts_heading_plurals( $number, $expected ) {
    $posts = $this->factory->post->create_many( $number );

    $this->expectOutput( $expected );

    recent_posts_heading( $posts );
}
```

Note:

* First thing, write a test to try to reproduce the issue
* Could write the test thusly:
    - @testWith annotation to specify 0, 1, or greater-than 1
    - Generate the given number of posts through a helper or factory we might have
    - Set expected output, since our function is printing directly
