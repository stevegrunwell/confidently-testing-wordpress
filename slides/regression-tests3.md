### Regression tests

<pre class="fragment-replacement"><code class="hljs lang-php fragment fade-out" data-fragment-index="0">function recent_posts_heading(array $posts) {
    if ( empty( $posts ) ) {
        _e( 'There have been no posts in the last 30 days.' );
    } else {
        printf(
            __( '%d posts in the last 30 days.' ),
            count( $posts )
        );
    }
}</code><code class="hljs lang-php fragment fade-in" data-fragment-index="0">function recent_posts_heading(array $posts) {
    if ( empty( $posts ) ) {
        _e( 'There have been no posts in the last 30 days.' );
    } elseif ( 1 === count( $posts ) ) {
        _e( 'One post in the last 30 days.' );
    } else {
        printf(
            __( '%d posts in the last 30 days.' ),
            count( $posts )
        );
    }
}</code></pre>

<pre class="fragment-replacement"><output class="fragment fade-out" data-fragment-index="0">0: <span class="pass"><span class="status-icon">&#x2714;</span> There have been no posts in the last 30 days.</span>
1: <span class="fail"><span class="status-icon">&#x1D5EB;</span> One post in the last 30 days.</span>
2: <span class="pass"><span class="status-icon">&#x2714;</span> 2 posts in the last 30 days.</span></output><output class="fragment fade-in" data-fragment-index="0">0: <span class="pass"><span class="status-icon">&#x2714;</span> There have been no posts in the last 30 days.</span>
1: <span class="pass"><span class="status-icon">&#x2714;</span> One post in the last 30 days.</span>
2: <span class="pass"><span class="status-icon">&#x2714;</span> 2 posts in the last 30 days.</span></output></pre>

Note:

* When we run our test, we start in a red state
* Our tests help push us towards another conditional, which makes our new test pass (green)
* If this function changes in the future, our test will break, alerting us to a regression
