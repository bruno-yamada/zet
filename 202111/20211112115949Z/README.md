# Building event-driven serverless applications 

DRAFT

Considerations:
- Idempotency
  - functions must not repeat an action, like adding a duplicate record to a
    database, reprocessing a file, or increase a counter twice
    - usually involves one of few approaches:
      - checking before the execution of any action, to see it has already been
        executed, but it can add significant overhead to the execution time
      - use idempotent functions when possible, like "InsertIfNotExists"
      - make it that even if the functions is executed in duplicate, the
        application can handle multiple duplicate records, or executing a
        function more than once doesn't affect the ending result.
- Timeouts:
  - You can define a timeout for your overall serverless function, but having a
    500 be returned to the user might not be as useful as more insightful error
    message, instead, when possible, define proper timeouts within the internal
    calls of the function, such as connecting to a database, making an http request
    and so forth
- Performance:
  - Be mindful of scope, variables/functions that are used often over the
    execution of the serverless function, should be done in a way that it
    doesn't need to be initialized or interpreted multiple times of the course of a
    exeuction


> tags: serverless; event-driven; idempotency;

> uid: 20211112115949Z

> links: 

