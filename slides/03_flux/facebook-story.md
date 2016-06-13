## Once upon a time ...

<img width="800"
     alt="Message Notification Icon Bug"
     src="slides/03_flux/images/facebook-message-notification.png">


<img width="800"
     class="fragment"
     alt="Really sad Zuckerberg"
     src="slides/03_flux/images/mark-zuckerberg-sad-fix-chat.jpg">

- UI inconsistencies in Facebook chat

<div class="slide-comment">
 - why are so many people interested in Flux nowadays?
    - Facebook (a *complex, supposedly reactive* application) had trouble with chat (2013?)
    - for weeks, the team was fighting to get the chat notification bubble to sync with the small chat window in the lower right corner.
    - often you'd visit Facebook and be happy about a *new message* indicator, only to be immediately disappointed after actually clicking the icon.
    - Even when totally unrelated features were announced, people just chimed "Fix Chat"!

 - Background:
    - Distributed (redundant) state in React components
    - Hey, the users are actually demanding a better architecture.
    - nah, they just want chat to work -- but the architecture is the way to do it!
</div>
