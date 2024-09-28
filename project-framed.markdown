---
layout: framed
title: FRAMED - moyevka
permalink: /framed/
---

<div class="container">
    <div class="container-item" style="align-items:center">
        <a href="https://framedsc.com/index.htm" target="_blank" style="width:80%">
            <img src="/assets/framed/svg/FramedLogoLarge.svg" title="visit the site!" class="glow-hover">
        </a>
    </div>
    <div class="container-item" style="align-items:center;text-align:left">
        <p class="framed fcard" style="width:80%;margin-top:18pt">I occasionally freelance for FRAMED, an online video game screenshotting community. Building upon existing cues, I worked on a cohesive theme for their site and overall appearance. I continue to contribute graphics as well as some technical writing every now and then.</p>
    </div>
</div>

{% assign posts = site.framed | sort: "title" %}
{% for post in posts %}
<!-- split -->
{{ post.content | raw }}
{% endfor %}