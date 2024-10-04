---
layout: naps
title: the naps! project - moyevka
permalink: /naps/
---

<style>
    .polyblock {
        width: auto;
        height: 128px;
        aspect-ratio: 4 / 1;
    }
    .textblock {
        max-width: 320px;
    }
    .voiceblock {
        display: flex;
        justify-content: center;
        background: transparent;
    }
@media (min-resolution: 144dpi) and (max-aspect-ratio: 1/1) {
    .polyblock {
        height: auto;
        width: 90%
    }
    .naps-title.poly {
        font-size: 15cqw;
        margin: 0;
    }
    .voiceblock {
        width: 80%;
        background:white;
        transform: translate(0, 2px);
    }
    .textblock {
        max-width: unset;
        width: 80%;
        background: white;
    }
}  
</style>

<div class="container" style="max-width:1200px">
    <div class="container-item" style="max-height:67vh;padding:0;align-items:center">
        <img src="/assets/naps/thegirls-promo.png" title="the girls!" class="naps-img" style="z-index:-1;max-height:none">
    </div>
    <div class="container-item footer" style="align-items:center">
        <div class="polyblock outlined">
            <div class="naps-polygon">
                <p class="naps-title poly" style="color:white; position:relative; top:-5%">
                    naps!
                </p>
            </div>
        </div>
        <div class="voiceblock">
            <p class="random-voice binary outlined" style="white-space:nowrap;margin:18px;margin-top:21px">
                "Everybody needs a nap!"
            </p>
        </div>
        <div class="textblock">
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