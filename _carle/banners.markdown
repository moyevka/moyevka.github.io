---
title: 02-carle
layout: carle
tags: design
---

<div class="section">
<style>
  .image-gallery {
    padding-top:5vh;
    padding-bottom:5vh;
  }
  .gallery-item {
    filter: drop-shadow(2px 2px 4px black);
    transition: all 0.1s;
    scale: 100%;
    margin-bottom:1vh
  }
  .gallery-item:hover {
    scale: 101%;
    filter: drop-shadow(4px 4px 8px rgba(0,0,0,0.5));
  }
  @media (max-width: 1200px) {
    .image-gallery {
      margin-top:50vh;
      padding-top:0;
      padding-bottom:40vh;
    }
    .container-item.header {
      height:25vh;
    }
  }
</style>

<svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" style="position:absolute;display:flex;justify-content:center;z-index:-1">
  <defs>
    <radialGradient id="carle-SpotlightBlack" cx="50%" cy="0%" r="100%" fx="50%" fy="0%">
      <stop offset="0%" style="stop-color:#575757; stop-opacity:1" />
      <stop offset="100%" style="stop-color:#2f2f2f; stop-opacity:1" />
    </radialGradient>
  </defs>
  <rect width="100%" height="100%" fill="url(#carle-SpotlightBlack)" />
</svg>

<div class="container" style="gap:5vh">
    <div class="container-item" style="align-items:center">
        <div class="image-gallery" style="scroll-snap-type:unset">
            {% assign images = site.static_files | where: "image", true | sort: "name" | reverse %}
            {% for image in images %}
                {% if image.path contains 'carle/banners/' %}
                    <div class="gallery-item" style="max-width:90%;border-radius:5pt">
                        <img src="{{ image.path }}" alt="{{ image.name }}" class="clickable carle-img" style="max-height:unset;width:100%;border-radius:5pt">
                    </div>
                {% endif %}
            {% endfor %}
        </div>
    </div>
    <div class="container-item header" style="z-index:2;justify-self:center">
        <p class="carle title white-text" style="margin:0">BANNERS</p>
        <p class="carle white-text" style="text-align:left;text-align-last:unset">In addition to the static ads, I was tasked with designing two standing banners that were placed outside the showroom.</p>
    </div>
</div>
</div>