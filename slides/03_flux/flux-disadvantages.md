## Disadvantages of Flux

*compared to "classic" MVC (AngularJS, Backbone)*

- each store *sees all actions*
- hard-wired *store-dependencies*
- stores are (conceptually) *singletons*
- *anti-pattern:* transporting *mutable state* in actions


<div class="slide-comment">
  - when triggering an action, it's not obvious which stores might be affected
  - stores know each other's APIs (for querying) and behaviour (waitFor)
  - waitFor may cause Deadlocks or endless recursion, but without waitFor
    implicit ordering sensitivity may occur (race-conditions-like).
  - singletons: alright, now I'd like to have *two product lists* - oh
  - *Mutable State in Actions:* apply discipline, extensive testing (deepFreeze)
    or libraries such as Immutable.JS.
  - *Local, transient state:* How to program e.g. drag/drop if UI is stateless?
    Don't be religious, determine which part of the UI state is actual business state.
</div>
