## Redux


<span class="fragment redux-overview-flux-overview">
<span style="position: absolute;">Flux:</span>
![Flux Flow](slides/03_flux/images/flux-overview.svg)
</span>
![Redux Flow](slides/04_redux/images/redux-overview.svg)




<div class="slide-comment">
- Let's have a look at the Redux core components: *View, Actions, Store, Reducers*
- As a *frame of reference*, let's revisit the Flux diagram that we've seen before
- Again, assume everything is *run on the client*

- *View:*
  - Again, React is used for the view layer
  - keeping local state would break the pattern
  - as with flux, the view is notified to rerender whenever the application
    state is modified.

  - Note: actions are created *and* dispatched by the view:

- *Actions:*
  - *action creators* are simply pure function that produce a description of a user's intent
  - in general, they must not have side effects
  - however, it's possible to create actions *asynchronously* by using an appropriate *middleware*
  - this allows you to e.g. talk to a REST API, and trigger an action only after the result arrives

- *Store:*
  - In contrast to Facebook Flux, there *a single state tree* in the application, and consequently exactly one store -- eliminating the need for a dispatcher.
  - Responsibility is not divided among *stores* (which *contain and manage* a slice of the application state), but among *reducers* which *transform a subtree of the state*. For their subtree of the state, they should be able to understand all relevant actions.

- *Reducer:*
  - The *root reducer* knows which sub-reducers to use for the top-level branches of the state tree, so it's application specific (in contrast to the Flux dispatcher, which is generic).
  - The sub-reducers may in turn divide their work and so on, forming a call-tree of their own.
  - The root reducer *returns a complete, new, transformed state tree* without touching the old state. If nothing has changed (most of the time), the reducer simply returns the old sub-tree unchanged.
  - If the store holds on to previous states, these snapshots can be used for a trivial undo/redo functionality.

</div>
