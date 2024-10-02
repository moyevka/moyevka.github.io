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

<div class="pageend" style="min-height:unset;height:auto;width:960px;max-width:90%;display:flex;justify-content:space-between;flex-direction:row;margin:0 auto;margin-bottom:14pt;overflow:visible">
    <div class="endtext" style="display:flex;flex-direction:row;width:100%;padding-top:0;padding-bottom:0;justify-content:space-between;align-items:center">
        <p class="binary">Enjoy Your Time!!!</p>
        <p class="binary" style="text-align:right">naps! by moyevka</p>
    </div>
</div>