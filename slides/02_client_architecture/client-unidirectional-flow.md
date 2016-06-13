## Unidirectional Flow

<img width="800"
     alt="unidirectional flow"
     src="slides/02_client_architecture/images/unidirectional-flow.svg">





<div class="slide-comment">
- Recently (with facebook publishing flux), UF has become popular as a simple interaction concept
- In principle, its not that different from "old-school" form based web applications (we've been using them for 20 years)
  - Server renders data model to HTML
  - User edits data using a form, POSTs it with to the server using a form-action
  - Server performs an action to modify its data store
  - Server renders new HTML

 - Why not do most of these steps completely client side, reducing download- and re-rendering time?
 - Only do on the server, what has to be done on the server (validation, storage)
 - Virtual DOM (e.g. React) makes this possible, as it makes it "cheap" to re-render everything on the client.

 - Combine
   - *architectural simplicity* of the old web (*addresses complexity goal*)
   - *responsiveness* of client-side applications (*addresses reactivity goal*).

 - NEXT: what does this look like in practice? And how to address the *scalability* goal?
</div>


Note:
- Grundlage für reaktive Frontendansätze
- schon lange bekannt in "normalen" Formularen
- ermöglicht durch virtuelles DOM (React)
- Gegenrichtung ausgeschlossen
