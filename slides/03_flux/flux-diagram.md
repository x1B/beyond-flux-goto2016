## Flux

<img class="main" src="slides/03_flux/images/flux-overview.svg" title="Flux Overview" />

<div class="slide-comment">
 - First, *Flux* is not a Library, or really even a framework: it's an architectural pattern
   (implemented by Facebook as a framework)
 - the result of the architectural overhaul undertaken at facebook,
   as a *recipe to build new applications.*

 - The core principle: *unidirectional flow*, which we've seen before
 - *First*:
   - Let's assume that for now, that all of this is running in the web browser
   - Server: just a provider of REST APIs

 - *What are the parts of a Flux application:*

 - *View*
   - A *Composite structure of JavaScript-Components*, that produce the HTML
     DOM which we can see on the screen and interact with. Usually (but not
     necessarily) React.
   - *No local application state* in the view. Rendering is always based on
     an application state that's *stored* elsewhere.
   - *Virtual-Dom-technology* such as React is especially applicable here,
     as it *efficiently* re-renders everything (no need to try and optimize
     model watchers as in AngularJS).

 - Actions and *Action Creatore*:
   - View never changes state directly, it always dispatches an action to do so.
   - An action encodes a *modification* to the application state,
     (usually) based on user intent. It has a *type* and may have a *payload*.
   - *Action Creators* help to create and schedule actions. For this, they may
     first asynchronously query a (REST) API, and then dispatch the action to the
     stores.
   - Usually, this entails action validation (locally and based on service responses).
   - Instantiated actions are passed to the *Dispatcher* for execution against the
     application state.
   - Related server-side concept: *CQRS* (Command/Query-Responsibility-Segregation).

  - The *Dispatcher*:
    - Passes each action to each registered store.
    - It does a bit more, so it's usually provided by a *flux implementation*.

  - Die *Stores*:
    - Stores actually run the actions to modify the application state accordingly.
    - State is *divided* among stores, which may query their peers for parts of the
      state that they do not own.
    - Stores allow all other components to *query* their state (views components,
      action creators, other stores).
    - So, each store knows about all other stores, and can observe all actions!
    - Usually, each store exists only once within an application:
      Actually, they were conceived as *singletons*, an only server-side rendering
      turned them into objects.
    - Once all stores have handled their actions, they notify their observing
      view components, which then re-render.

   NEXT: alright, I am sold, where can I download this?
</div>
