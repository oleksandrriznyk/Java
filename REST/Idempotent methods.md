### Idempotent Methods

The term idempotent is used more comprehensively to describe an  **operation that will produce the same results if executed once or multiple times**. This is a very useful property in many situations, as it means that an operation can be repeated or retried as often as necessary without causing unintended effects. With non-idempotent operations, the algorithm may have to keep track of whether the operation was already performed or not.

In HTTP specification, The methods  **GET, HEAD, PUT and DELETE are declared idempotent methods**. Other methods OPTIONS and TRACE SHOULD NOT have side effects so both are also inherently idempotent.
