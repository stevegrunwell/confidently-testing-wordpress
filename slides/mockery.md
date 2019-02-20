### [Mockery](http://docs.mockery.io/)

Popular library for creating test doubles:

```php
public function test_handles_empty_order_list() {
    $api = Mockery::mock( Api::class )->makePartial();
    $api->shouldReceive( 'get_all_orders' )
        ->once()
        ->andReturn( [] );

    $this->assertEmpty( $api->get_recent_orders() );
}
```
<!-- .element: class="fragment" -->

Note:

* While PHPUnit allows for some test doubles, Mockery is a popular alternative
    - Expressive interface for defining test doubles, their expectations, and responses
* API object should receive get_all_orders() exactly once and return an empty array
    - Will fail the test if get_all_orders() isn't called exactly once
