---
layout: naps
title: 01-naps
tags: illustration, design
---

<div class="image-gallery" style="width:100%">
    <div class="gallery-item gallery-header">
        <p class="naps-title" style="font-style:normal">meet the girls!</p>
        <p class="binary">get to know Mara, Sorrel, Choux, and Keys: the 4 main characters of the naps project. each of these sheets aims to explore each character's personality through distinct visual themes, such as colour, background and fashion choice.</p>
    </div>
    {% assign images = site.static_files | where: "image", true | sort: "name" %}
    {% for image in images %}
        {% if image.path contains 'naps/meet-the-girls' %}
            <div class="gallery-item">
                <img src="{{ image.path }}" alt="{{ image.name }}" class="clickable naps-img">
            </div>
        {% endif %}
    {% endfor %}
</div>