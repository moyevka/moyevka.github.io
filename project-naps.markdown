---
layout: naps
title: the naps! project - moyevka
permalink: /naps/
---

<div class="container" style="max-width:1200px">
    <div class="container-item" style="max-height:67vh;padding:0;align-items:center">
        <img src="/assets/naps/thegirls-promo.png" title="the girls!" style="z-index:-1;max-height:none;image-rendering:pixelated">
    </div>
    <div class="container-item footer" style="align-items:center">
        <div class="outlined" style="width:440px;height:128px">
            <div class="naps-polygon">
                <p class="naps-title" style="color:white; position:relative; top:-5%">
                    naps!
                </p>
            </div>
        </div>
        <P class="random-voice binary outlined" style="white-space:nowrap;margin:18px;margin-top:21px">
            "Everybody needs a nap!"
        </p>
        <div style="max-width:320px">
            <p class="binary outlined" style="margin-left:12px;margin-right:12px;margin-top:6px;margin-bottom:6px">
                naps is my pet project, where I explore and practice my design & typography skills to accompany illustrations of my characters along with some extra friends!
            </p>
        </div>
    </div>
</div>

{% assign posts = site.naps | sort: "title" %}
{% for post in posts %}
<!-- split -->
{{ post.content | raw }}
{% endfor %}