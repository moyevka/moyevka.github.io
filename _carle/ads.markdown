---
title: 01-carle
layout: carle
tags: design
---

<svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" style="position:absolute;display:flex;justify-content:center;z-index:-1">
  <defs>
    <radialGradient id="grad1" cx="50%" cy="0%" r="100%" fx="50%" fy="0%">
      <stop offset="0%" style="stop-color:#fccc85; stop-opacity:1" />
      <stop offset="100%" style="stop-color:#FC9800; stop-opacity:1" />
    </radialGradient>
  </defs>
  <rect width="100%" height="100%" fill="url(#grad1)" />
</svg>

<p class="carle title white-text" style="z-index:9999;pointer-events:none">AD DESIGNS</p>
<p class="carle white-text" style="z-index:9999;pointer-events:none">designed in Illustrator <br> copywriting done by marketing</p>

<p class="carle subtitle orange" style="position:absolute;top:14pt"><span style="font-weight:800;color:black">CLICK & HOLD</span> to drag images around, <span style="font-weight:800;color:black">CLICK ONCE</span> to inspect.</p>

<div class="post-gallery" id="scatterPlace">
    {% assign images = site.static_files | where: "image", true | sort: "name" | reverse %}
    {% for image in images %}
        {% if image.path contains 'carle/ads/' %}
            <div class="post-item">
                <img src="{{ image.path }}" alt="{{ image.name }}" class="movable clickable carle-img" style="border-radius:5pt">
            </div>
        {% endif %}
    {% endfor %}
</div>