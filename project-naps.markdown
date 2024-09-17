---
layout: naps
title: home
permalink: /naps/
---

<div class="container" style="max-width:1200px">
    <div class="container-item" style="max-height:100vh;padding:0">
        <img src="/assets/naps/thegirls-promo.png" title="the girls!" style="z-index:-1;max-height:none;image-rendering:pixelated">
    </div>
    <div class="container-item footer">
        <div style="width:440px;height:128px;filter:url(#binary) drop-shadow(4px 4px 0 #fff) drop-shadow(-4px 4px 0 #fff) drop-shadow(-4px -4px 0 #fff) drop-shadow(4px -4px 0 #fff)">
            <div class="naps-polygon">
                <p class="naps-title" style="color:white; position:relative; top:-5%">
                    naps!
                </p>
            </div>
        </div>
        <P class="random-voice binary" style="white-space:nowrap;margin:18px;margin-top:21px">
            "Everybody needs a nap!"
        </p>
        <div style="background:white; max-width:320px">
            <p class="binary" style="margin-left:12px;margin-right:12px;margin-top:6px;margin-bottom:6px">
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