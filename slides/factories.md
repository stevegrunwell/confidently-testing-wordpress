### Factories <!-- .element: class="wordpress-icon" -->

Generate users, posts, and more for testing.

<pre class="hljs"><code class="hljs lang-php fragment">// Create the post and retrieve its ID.
$post_id = $this->factory->post->create();
</code>
<code class="hjls lang-php fragment">// Create and retrieve the new post.
$post = $this->factory->post->create_and_get();</code>
<code class="hljs lang-php fragment">// Override default parameters.
$post = $this->factory->post->create_and_get( [
    'post_title'  => 'My Test Post',
    'post_author' => $author_id,
] );</code>
<code class="hljs lang-php fragment">// Create multiple instances.
$posts = $this->factory->post->create_many( 5, [
    'post_author' => $author_id,
] );</code></pre>

Note:

Factories, which are included in the core test suite, let us easily generate test data (posts, users, comments, terms, attachments, and more).

The create method will return the object_id, while create_and_get() will return the generated object.

We can also override default arguments by passing an array.

Need to create an author with five posts? It's two lines.
