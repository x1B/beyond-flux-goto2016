## Reactivity & Responsiveness

- synchronize state (across devices)
- provide immediate feedback
- continuous bi-directional communication (client/server)

<p>&nbsp;</p>

*http://www.reactivemanifesto.org*




<div class="slide-comment">
- applications are expected to work on multiple devices, with seamless synchronization
- e.g. twitter: when I post a tweet from my phone, my laptop should reflect this right away

- people have come to expect immediate feedback
- users expect to perform search or validation without having to click a button first
- server-interaction should be invisible and run in the background, avoiding unnecessary reloads and confirmation pages
- ideally, apps even compensate for services being slow or unavailable (fake the UI result of an interaction, roll back if it turns out that the action cannot be carried out).

- This means that web apps are about more than just regular HTML pages connected through links (those will not go away) and pulling content updates through ajax calls
- instead: communication happens in real time
- client may at any time push to server (user input, metrics, ...)
- server may at any time push to client (other devices, social peers, feed updates, ...)

- NEXT: now that we've looked at architecture from a user POV, what's important for developers or development teams?
</div>

Note:
1. Cross-Device synchronization
2. Immediate feedback
3. Bidi-Push (plus traditional request/response)
