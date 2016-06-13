## PubSub in practice

![Logo LaxarJS](slides/05_pubsub/images/bulli.svg)

#### from event bus to framework
http://www.laxarjs.org
  - component configuration
  - lifecycle: *when are event collaborators available?*
  - services for view components:
    *where do I render my HTML to?*
  - development tools (event log, visual composition structure)



Note:
 - *Just event bus* would be similar to *just the flux dispatcher*
 - But the power is in the *topic configuration*.
 - Alternative:
   - Provide component bootstrapping
   - Declarative descriptor to explain the allowed configuration (JSON schema)
   - event-based navigation/routing
   - reuse view components across applications using themes
