---
order: 3
title: photocards
layout: naps
tags: illustration, design
---

<style>
    .pcards {
        max-width: 520px;
    }
@media (max-aspect-ratio: 1/1) {
    .pcards {
        max-width: 90%;
    }
}
</style>

<div class="container">
    <div class="container-item header" style="z-index:1">
        <p class="naps-title">photocards</p>
        <p class="binary pcards">click & hold to drag images around, click once to inspect. <br><br> a collection of portraits, each depicting different characters belonging to my friends. this was more of a hybrid project, as i wanted to experiment with dither conversion. behind the pixelation of each photocard is a digital painting that was then passed through multiple stages of dithering to achieve an end product i was satisfied with. each layer had to be processed individually as a wide range of colour present would cause odd colours like grey and green to spill into colours like skintones. <br><br> backgrounds were also heavily emphasised, probably constituting a third of the workload, as i really wanted to give each character a background that was unique and complimented them. <br><br> made in clip studio paint</p>
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