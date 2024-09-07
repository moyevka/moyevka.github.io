---
layout: naps
title: naps home
permalink: naps
---

<!-- columns -->

<img src="/assets/splash/thegirls-promo.png" title="the girls!" style="z-index:-1; margin-left:50%; transform:translateX(-50%); max-height:none">

<!-- column-break -->

<p class="naps-title" id="outlined">naps!</p>
<P class="random-voice binary" style="white-space:nowrap" id="outlined">
    "Everybody needs a nap!"
</p>
<p class="binary" style="max-width:320px" id="outlined">
    naps is my pet project, where I explore and practice my design & typography skills to accompany illustrations of my characters along with some extra friends!<br><br>some outline code has been added that fucks up the pixel-perfect rendering lol
</p>



{% assign posts = site.naps | sort: "title" %}
{% for post in posts %}
<!-- split -->
{{ post.content | raw }}
{% endfor %}