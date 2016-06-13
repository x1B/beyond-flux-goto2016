## Advantages of Flux

*compared to "classic" MVC (AngularJS, Backbone)*

- strict separation: State / UI / Behavior
- each value stored exactly once
- clear data flow, good testability
- server-side rendering relatively simple

<div class="slide-comment">
   - the central *value proposition* of Flux is that unidirectional flow and
     single store responsibility, ensures that the UI stays *consistent*,
     independent of which UI-part has triggered an action.

   - *testing components is simple, except* for stores that interact too much
     with each other (extensive mocking may be needed).

   - *Server side rendering* (using node.JS, nashorn) ist relatively
     simple: just render the components, and serialize the store state.
</div>
