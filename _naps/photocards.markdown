---
title: 03 naps
layout: naps
tags: illustration, design
---

<div class="container">
    <div class="container-item header">
        <p class="naps-title">photocards</p>
        <p class="binary">a collection of portraits, each depicting different characters belonging to my friends.</p>
        <p class="binary">click & hold to drag images around, click once to inspect.</p>
    </div>
    <div class="container-item">
    </div>
</div>

<div class="post-gallery" id="clusterPlace-randomSort">
    {% assign images = site.static_files | where: "image", true | sort: "name" | reverse %}
    {% for image in images %}
        {% if image.path contains 'naps/photocards/' %}
            <div class="post-item naps">
                <img src="{{ image.path }}" alt="{{ image.name }}" class="movable clickable naps-img">
            </div>
        {% endif %}
    {% endfor %}
</div>