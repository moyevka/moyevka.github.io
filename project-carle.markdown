---
layout: carle
title: carle
permalink: /carle/
---

<div class="vimeo-wrapper" style="filter:brightness(75%)">
<img src="../assets/carle/homepage.jpg" alt="Homepage Background" id="video-placeholder">
<iframe id="vimeo-video" src="https://player.vimeo.com/video/1008304143?background=1&autoplay=1&loop=1&byline=0&title=0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>

<script>
    const vimeoVideo = document.getElementById('vimeo-video');
    const videoPlaceholder = document.getElementById('video-placeholder');
    vimeoVideo.onload = function() {
        setTimeout(() => {
            videoPlaceholder.remove();
        }, 1000);
    };
</script>

<div>
<p class="carle" style="visibility:hidden">I interned at Carle for my final year in polytechnic. I worked closely with their marketing and media leads to produce static advertisements and short promotional videos for the automotive brand. I also helped to shoot & edit a long-form video for their YouTube channel.</p>
</div>
<div class="svg-background" style="display:flex;justify-content:center;width:100%;background-image:url(../assets/carle/svg/paint-1.svg);background-position-x:52%">
    <p class="carle title white-text" style="font-size:128pt;font-style:italic">CARLE</p>
</div>
<p class="carle white-text blur-box">I interned at Carle for my final year in polytechnic. I worked closely with their marketing and media leads to produce static advertisements and short promotional videos for the automotive brand. I also helped to shoot & edit a long-form video for their YouTube channel.</p>
<p class="carle subtitle white-text" style="position:absolute;bottom:14pt">ALL ASSETS ON THIS PAGE ARE AUTHORED BY ME, AND USED WITH PERMISSION.</p>
<p class="carle subtitle white-text blur-box" style="position:absolute;top:-6px;border-top-left-radius:0;border-top-right-radius:0;margin-top:0;padding-bottom:10pt">this homepage video was shot by me, licence plate removal done in Nuke.</p>

{% assign posts = site.carle | sort: "title" %}
{% for post in posts %}
<!-- split -->
{{ post.content | raw }}
{% endfor %}