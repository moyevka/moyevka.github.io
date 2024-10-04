---
title: 03-framed
layout: framed
tags: photography
---

<style>
  .post-item img {
    max-width:33vw;
    max-height:50vh;
    border-radius: 5pt;
    transition: all 0.1s ease;
  }
  .post-item img:hover {
    border-radius: 10pt;
  }
  .post-item {
    scale:98%;
    box-shadow: 0px 3px 5px rgba(0,0,0,0.5);
    border-radius: 5pt;
  }
  .post-item:hover {
    box-shadow: 0px 0px 10px rgba(0,0,0,0.5);
    border-radius: 10pt;
  }
  .hofcard {
    line-height: 21pt;
  }
@media (min-resolution: 144dpi) {
  .hofcard {
    line-height: unset;
    max-width: 92vw;
    margin-left: 4vh;
    margin-right:4vh;
  }
}
</style>

<div class="fcard" style="z-index:100;padding-bottom:0">
<p class="framed title" style="font-size:48pt;text-align:center">VIRTUAL PHOTOGRAPHY</p>
<p class="framed" style="text-align:center">some of my own screenshots that I've taken as part of FRAMED <br> postprocessed with Nuke</p>
</div>

<p class="framed fcard viewer" style="z-index:100;position:absolute;top:14pt;padding-top:7pt;padding-bottom:7pt">CLICK & HOLD to drag images around, CLICK ONCE to inspect.</p>
<p class="framed fcard hofcard" style="z-index:9999;position:absolute;bottom:14pt;padding-top:7pt;padding-bottom:7pt">View more screenshots from the rest of FRAMED!<br> 
<a href="https://framedsc.com/HallOfFramed/" target="_blank" style="width:100%">
  <img src="/assets/framed/svg/HoFLogo.svg" title="Hall of FRAMED" class="glow-hover">
</a>
</p>

<div class="post-gallery" id="columnPlace-randomSort">
    {% assign images = site.static_files | where: "image", true | sort: "name" | reverse %}
    {% for image in images %}
        {% if image.path contains 'framed/vp/' %}
            <div class="post-item">
                <img src="{{ image.path }}" alt="{{ image.name }}" class="movable clickable framed-img">
            </div>
        {% endif %}
    {% endfor %}
</div>