## Disadvantages of Redux

*vs. "vanilla" Flux*

- must protect against mutating state, using e.g.
   - spread constructor `{...oldState, prop: newVal}` (ES201?)
   - (test with) recursive `Object.freeze()`
   - Immutable.js
- potentially steep learning curve (functional paradigm)
- container components know the whole state tree




<div class="slide-comment">
- if state is manipulated directly (strongly discouraged),
  most advantages go out of the window
  - ES2015 array-spread and ES2016 object spread do help
  - but actual protection against accidental state manipulation is needed.
  - Builtin-mechanisms prohibitively slow, but recursive
    `Object.freeze` is useful for testing reducers.
    If used, any attempted state mutation leads to an error.

- For pure functional data structures, Immutable.js can be used.
  Prevents state mutation, and provides immutable set, record...
  But, it's just not as straightforward as native JS objects.

- functional paradigm: not giving you my opinion, but it may
  require some adjustments.
  - especially for web developers, applying a mathematical
    model to programming may not be straightforward.
  - seeing reload/replay in action may convince some people

- The redux `connect` call always passes the complete state to
  all "top-level" components.
  - It is not obvious, which components work with what parts of the state (in Flux, you have subscribe calls to various stores).
  - Refactoring something in the state might affect any component in your application.

- it does what Flux does, but (arguably) better
</div>
