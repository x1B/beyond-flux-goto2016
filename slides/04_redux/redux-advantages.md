## Advantages of Redux

*vs. "vanilla" Flux*

- functional composition
- snapshot/replay capabilities
- can yield performance boost
  (free dirty-checking)




<div class="slide-comment">
- a sequence of actions plus starting state deterministically
  leads to a goal state
  - simple undo/recovery (either snapshotting or replay to n-1)
  - simple bug identification
  - simple state tracing (e.g. for metrics)

- The critical logic is combined from pure functions,
  which are very easy to test
  - no side-effects to provoke / check, nothing to mock
  - just provide input, check output
  - Also: hot code reload can be reasoned about
    - re-apply action sequence using swapped-out reducer tree

- the view layer can simply check for object identity,
  no change listener needed:
  - if a branch of the state tree is referentially
    the same as last time, nothing needs to be re-rendered for
    that branch
</div>

Note:
1. Nur initialer Zustand und Aktionsfolge benötigt
2. Reine Funktionen:
    - Reducer sehr leicht testbar
    - Hot code reloading
3. kostenloser Dirty-Check über Objektidentität
