### Test Doubles

<dl>
    <dt>Stub</dt>
    <dd>Set the response values</dd>
    <dt>Mock</dt>
    <dd>Replace an object with one that verifies expectations</dd>
    <dt>Spy</dt>
    <dd>Similar to a mock, but tracks what has happened</dd>
</dl>

Note:

* Terms that get thrown around a lot
* Stub: Hard-code the response for a function/method
    - Very useful for API responses
    - Pretty easy to implement via WordPress filters
* Mock: Verify that an object behaves in a certain way
* Spy: Observe what has happened
    - Expect this to happen v. assert that this did happen
