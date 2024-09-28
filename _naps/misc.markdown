---
title: 04 naps
layout: naps
tags: illustration
---


<p class="naps-title">miscellaneous</p>
<p class="binary">all my other illustrative work related to the naps project.</p>
<p class="binary" style="visibility:hidden">br</p>
<p class="binary">click & hold to drag images around, click once to inspect.</p>


<div class="post-gallery" id="columnPlace">
    {% assign images = site.static_files | where: "image", true | sort: "name" | reverse %}
    {% for image in images %}
        {% if image.path contains 'naps/misc/p/' %}
            <div class="post-item naps">
                <img src="{{ image.path }}" alt="{{ image.name }}" class="movable clickable naps-img">
            </div>
        {% elsif image.path contains 'naps/misc/' %}
            <div class="post-item">
                <img src="{{ image.path }}" alt="{{ image.name }}" class="movable clickable naps-img">
            </div>
        {% endif %}
    {% endfor %}
</div>

<div class="pageend">
    <div class="endtext">
    <p class="binary">Enjoy Your Time!!!</p>
    <p class="binary">naps! by moyevka</p>
    </div>
</div>