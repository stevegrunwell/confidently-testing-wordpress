### Negative Assertions

<table class="equivalence-table">
    <tr class="fragment">
        <td><code>assertEquals()</code></td>
        <td><code>assertNotEquals()</code></td>
    </tr>
    <tr class="fragment">
        <td><code>assertContains()</code></td>
        <td><code>assertNotContains()</code></td>
    </tr>
    <tr class="fragment">
        <td><code>assertArrayHasKey()</code></td>
        <td><code>assertArrayNotHasKey()</code></td>
    </tr>
    <tr class="fragment">
        <td><code>assertCount()</code></td>
        <td><code>assertNotCount()</code></td>
    </tr>
</table>

&hellip;etc.<!-- .element: class="fragment" -->

Note:

* (Most) every assertion has an equal and opposite assertion
    - Typically in the form of assertThing(), assertNotThing()
