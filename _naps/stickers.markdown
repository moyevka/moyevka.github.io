---
title: 02-naps
layout: naps
tags: illustration, design
---

<!-- columns -->

<p class="naps-title">stickers</p>
<p class="binary">made in under a weekend each, these 'stickers' are the ground zero for the naps project. a combination of illustration, design & typography packaged in 1-bit 512x512 images.</p>

<!-- column-break -->

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