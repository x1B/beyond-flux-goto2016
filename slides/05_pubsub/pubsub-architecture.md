## PubSub Architecture

![pub-sub-overview](slides/05_pubsub/images/pub-sub-overview.svg)

- event bus: connects senders/receivers (asynchronously)

- *view components,* like in Flux/Redux (+ create action events)

- *activity components,* like Flux stores (+ completion of async actions)

- unidirectional flow using event patterns


Note:
  - Pub/Sub *as a generalization* of flux:
    - event bus is a dispatcher that offers multiple topics (message channels)
    - like Flux actions, events have name and payload
    - for *scalability* we determined that topics should not be constants, but should be *configurable*
    - *event subscriptions* work similarly to observables

  - So, what about action creators?
    - *Intent* is specified by the view components publishing an action event.
    - *Handling* (including async API requests) happens in the activity components

  - Messages vs. Events: Events describe *what happened* ("user *has* added this article to the shopping cart", "this resource just came from the server").
    - events do not indicate what the recipient should do with them

  - For *UDF* we define higher level collaborations on top of pub/sub:
    - *resources:*
      - are published whenever they have been received/modified
    - *action events:*
      - *view publishes a request-event* with intent+payload,
      - *activities say* "I'll do something", then performs async processing (e.g. REST)
      - finally *activities publish a response* including outcome (success/error)
