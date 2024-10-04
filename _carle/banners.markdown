---
title: 02-carle
layout: carle
tags: design
---

<div class="section" style="background: radial-gradient(ellipse at top, #e8dccf, #c0ae9b, #918477, #625d57, #373737)"> 
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
  .carle.title.white-text.banners {
    margin:0;
  }
  @media (max-aspect-ratio: 1/1) {
    .image-gallery {
      margin-top:55rem;
      padding-top:0;
      padding-bottom:50rem;
    }
    .carle.title.white-text.banners {
      margin-bottom: 5rem;
    }
  }
</style>

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
        <p class="carle title white-text banners">BANNERS</p>
        <p class="carle white-text" style="text-align:left;text-align-last:unset">In addition to the static ads, I was tasked with designing two standing banners that were placed outside the showroom.</p>
    </div>
</div>
</div>