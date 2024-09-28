---
title: 02 naps
layout: naps
tags: illustration, design
---

<div class="container">
    <div class="container-item" style="align-items:center">
        <div class="image-gallery">
            {% assign images = site.static_files | where: "image", true | sort: "name" | reverse %}
            {% for image in images %}
                {% if image.path contains 'naps/stickers/' %}
                    <div class="gallery-item">
                        <img src="{{ image.path }}" alt="{{ image.name }}" class="clickable naps-img">
                    </div>
                {% endif %}
            {% endfor %}
        </div>
    </div>
    <div class="container-item header" style="z-index:2;background:white;padding:48px">
        <p class="naps-title">stickers</p>
        <p class="binary">made in under a weekend each, these 'stickers' are the ground zero for the naps project. a combination of illustration, design & typography packaged in 1-bit 512x512 images, they were born from experiments with a low fidelity artstyle that could be done quickly and still presented as punchy and distinct. i started to really lean into these during my time in national service, where i was only afforded a weekend of free time to pursue my hobbies. <br><br> made in clip studio paint, illustrator</p>
    </div>
</div>

