### Data providers

<pre class="fragment-replacement"><code class="hljs lang-php fragment fade-out" data-fragment-index="0">/**
 * @dataProvider my_data_provider()
 */
public function test_my_function( $expected, $value ) {
    $this->assertEquals( $expected, my_function( $value ) );
}

public function my_data_provider() {
    return [
        'Description of case 1' => ['foo', 'bar'],
        'Description of case 2' => ['bar', 'baz'],
    ];
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="0">/**
 * @testWith ["foo", "bar"]
 *           ["bar", "baz"]
 */
public function test_my_function( $expected, $value ) {
    $this->assertEquals( $expected, my_function( $value ) );
}</code></pre>

Note:

* Lets you pass multiple variants to the same test method
* @dataProvider tag lets you reference another method, which should return an array of scenarios
* Can also use @testWith and pass them directly in the DocBlock
    - Cannot call functions or use constants
