---
title: 01-carle
layout: carle
tags: design
---

<div class="section" style="background: radial-gradient(ellipse at top, #fccc85, #fc9800)">

<p class="carle title white-text" style="z-index:100;max-width:50%">AD DESIGNS</p>
<p class="carle white-text" style="z-index:100;max-width:50%">designed in Illustrator <br> copywriting done by marketing</p>

<p class="carle subtitle orange" style="position:absolute;top:14pt;z-index:100"><span style="font-weight:800;color:black">CLICK & HOLD</span> to drag images around, <span style="font-weight:800;color:black">CLICK ONCE</span> to inspect.</p>

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
</div>