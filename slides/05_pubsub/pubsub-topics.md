### PubSub Architecture

## Topics for Scalability

![pub-sub-topics](slides/05_pubsub/images/pub-sub-topics.svg)

- topics for *resources* (state slices) and *actions* (intents to modify)

- topics connect components in a *configurable* way


Note:
 - distinct *topics isolate components*, define namespaces as you like (different from Flux)
 - shared *topics connect components*.
   If done solely through configuration, the paths of communication become visible and inspectable.
 - *Scalability:* This allows to any number of "applications" to live side by side within a browser window, and also to talk to each other (portal-style scenarios).
