# Why Architecture?

## It's about time!

<img width="800"
     alt="JS Transfer Size Chart"
     src="slides/02_client_architecture/images/js-transfer-chart.svg">

*(Source: httparchive.org)*

<p>&nbsp;</p>

- We are *building* complex software *(requires tools)*,
- and we are *talking* about them *(requires a language)*.




<div class="slide-comment">
- 100kB to 400kB JS in 5 years, in spite of better minification
- Assume an average site may have 10s to 100s kLoC JS
- not having an architecture makes it hard to find bugs, add features
- several developers, or even several teams
- gone are the olden times of sprinkles of jQuery to add some fancyness at the end

- how do structure these things as we build them? How do we talk about them?

- NEXT: so, what are the things we'd like our architecture to do?
</div>


Note:
- JS-Transfer wächst linear trotz besserer Minifizierung
- Typisch >>100k LOC
- Steigende Komplexität
- Vom Bastler zu Frontend-Teams
