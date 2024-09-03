---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: moyevka!
tags: [personal, illustration, design]
test: moyevka!
---

<p class="binary">{{ page.test }}</p>

<!-- split -->

<!-- bg: ./assets/splash/naps-splash.png -->

<p><a href="/naps/" class="naps-title outlined">naps!</a></p>  

<!-- tagblock -->

<!-- split -->

<p class="binary">i also have one more problem i haven't solved in a wholly satisfying way yet, which is how paragraphs are being handled. since i obviously want some text wrapping to occur, there's a `max-width` set, however when text wraps this forces the element to be set to the max-width instead of to the bounds of the text. i found some javascript[1] that retroactively sets the width of the element to the bounds of the text, but same with the js from earlier it's not a dynamically stable approach and breaks when the viewport is resized. i don't think this is a big concern though but i'm not sure.</p>

<!-- split -->

e