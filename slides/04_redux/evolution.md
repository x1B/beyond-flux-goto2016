### Redux

## The Evolution

### `(state, action) → state`




<div class="slide-comment">
- Although not the first UDF architecture, Flux has caused a kind of landslide
  in web frontend architecture.
- The most prominent offspring is called *Redux* and has started to outgrow
  Flux (at least in terms of buzz).
- Aside from flux, Redux is inspired by *Elm*, a functional compiles-to-js
  language that also uses a unidirectional flow.

- Redux expresses application behavior as a *sequence of state transitions*.
- Each of these transitions takes the current state, and the next action,
  to deterministically produce a new state.
- Each function that implements such a state transition is called a *reducer*.

- Based on an initial state, each application state can be reproduces by
  re-applying the action sequence that caused it.
  This makes tracking down bugs very simple!

- NEXT: let's have a look at the Redux architecture, and compare it to flux.
</div>
