---
title: 02-naps
layout: naps
---

<!-- columns -->

<p class="naps-title">stickers</p>
<p class="binary">made in a weekend each</p>

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