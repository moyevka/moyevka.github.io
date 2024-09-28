---
layout: carle
title: Carle - moyevka
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

<div class="snap"></div>

<div class="section">
    <div style="display:flex;flex-direction:column;justify-content:space-between;height:50vh;align-items:center">
        <p class="carle white-text blur-box" style="visibility:hidden;width:650px;max-width:80vw">I interned at Carle for my final year in polytechnic. I worked closely with their marketing and media leads to produce static advertisements and short promotional videos for the automotive brand. I also helped to shoot & edit a long-form video for their YouTube channel.</p>
        <img src="/assets/carle/svg/carle-logo.svg" class="carle-logo">
        <p class="carle white-text blur-box" style="width:650px;max-width:80vw">I interned at Carle for my final year in polytechnic. I worked closely with their marketing and media leads to produce static advertisements and short promotional videos for the automotive brand. I also helped to shoot & edit a long-form video for their YouTube channel.</p>
    </div>
    <p class="carle subtitle white-text" style="position:absolute;bottom:14pt;max-width:50%">ALL ASSETS ON THIS PAGE ARE AUTHORED BY ME, AND USED WITH PERMISSION.</p>
    <p class="carle subtitle white-text" style="position:absolute;max-width:50%;top:14pt">this homepage video was shot by me, licence plate removal done in Nuke.</p>
</div>

{% assign posts = site.carle | sort: "title" %}
{% for post in posts %}
<div class="snap"></div>
{{ post.content | raw }}
{% endfor %}