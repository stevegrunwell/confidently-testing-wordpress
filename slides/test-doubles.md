### Test Doubles

Replacing actual systems with test versions.

* Always return known values <!-- .element: class="fragment" -->
* Ensure systems behave a certain way <!-- .element: class="fragment" -->
* etc. <!-- .element: class="fragment" -->

Note:

Another talk in itself, but test doubles let us focus on our system under test and replace anything else with something we can easily control.

You might stub an API to make sure it always gives the type of response you're looking for, for instance. You're not testing the API, you're testing how your system handles different API responses.
