---
layout: naps
title: naps home
permalink: naps
---

<!-- columns -->

<P class="binary choux">"Everybody needs a nap!"</p>  
<p class="binary" style="max-width:320px">naps is my pet project, where I explore and practice my design skills to accompany illustrations of my characters, including some guests!</p>

<!-- column-break -->

<img src="/assets/splash/thegirls-promo.png" alt="the girls!" style="z-index:-1">

{% assign posts = site.naps %}
{% for post in posts %}
<!-- split -->
{{ post.content | raw }}
{% endfor %}