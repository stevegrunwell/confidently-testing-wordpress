### Test types

<dl>
    <dt class="fragment" data-fragment-index="0">Unit</dt>
    <dd class="fragment" data-fragment-index="0">Test the smallest possible unit of an app</dd>
    <dd class="fragment" data-fragment-index="1">Often a single function</dd>
    <dt class="fragment" data-fragment-index="2">Integration</dt>
    <dd class="fragment" data-fragment-index="2">How individual components interact</dd>
    <dt class="fragment" data-fragment-index="3">End-to-end (E2E)</dt>
    <dd class="fragment" data-fragment-index="3">An entire path through an application</dd>
</dl>

Note:

* Unit tests are often limited to a single function
    - Should not have dependencies on any other functionality
    - Does this function do what we expect?
* Integration testing, often called "feature" testing
    - Tests how the individual units come together
* End-to-end (or "full-stack" testing) test the full application
    - Often includes front-end tests via headless browsers
