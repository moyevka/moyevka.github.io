---
layout: home
title: moyevka!
tags: [personal, illustration, design]
test: moyevka!
---

<style>
    .section {
        scroll-snap-align:none;
        scroll-snap-stop:always;
        height:100vh;
        padding:0;
        position:sticky;
        top:0;
        max-width:100vw;
        overflow:visible;
        overflow-x:clip
    }
</style>

<div class="snap"></div>

<div class="section" style="background: linear-gradient(180deg, #f6f6f3 75%, #deddda 100%)">
    <div style="text-align:left;max-width:520px;color:#201010">
        <p style="font-style:italic;left:36pt;bottom:-8pt;position:relative;margin:0;font-size:20pt;letter-spacing:-0.05em"><i>oh hey! it's</i></p>
        <p style="margin:0;font-family:'PP Pangaia';font-size:96pt;line-height:0.6;letter-spacing:-0.05em">moyevka!</p>
        <br>
        <p>visual artist, graphic designer, whatever you wanna call it, <br> i just like to make stuff that looks cool. <br> let's create something together!</p>
    </div>
    <img src="/assets/splash/home-bottom.svg" class="homebg" style="width:auto;height:auto;position:absolute;bottom:0;left:0;z-index:-1">
    <img src="/assets/splash/home-top.svg" class="homebg" style="width:auto;height:auto;position:absolute;top:0;right:0;z-index:-1">
</div>

<div class="snap"></div>

<div class="section" style="background-image: url('/assets/splash/naps-splash.png'); background-color:white; min-height:100vh; background-repeat: no-repeat; background-position: center; background-size: auto 1325px; image-rendering: pixelated;filter:drop-shadow(0px 0px 2px rgba(32, 16, 16, 0.5))">
    <p class="main-text bottom-tab"><i>scroll down to see my work!</i></p>
    <p><a href="/naps/" class="naps-title outlined">naps!</a></p>  
</div>

<div class="snap"></div>

<div class="section" style="background:radial-gradient(ellipse at bottom, #fccc85 0%, #fc9800 100%);filter:drop-shadow(0px 0px 2px rgba(0,0,0,0.5))">
    <p class="carle title white-text bottom-tab" style="margin:0;font-size:18pt;background:#fc9800;letter-spacing:0em;text-shadow: 1px 1px 2px rgba(0,0,0,0.5);">CARLE</p>
    <a href="/carle/" class="carle title white-text" style="z-index:2">
        <img src="/assets/carle/svg/carle-logo-stack.svg" class="carle-logo hover">
    </a> 
    <div style="position:absolute;height:100%;width:100%;overflow:clip;display:flex;justify-content:center;align-items:center">
        <img src="/assets/carle/svg/paint-2.svg" style="filter:drop-shadow(2px 2px 4px rgba(0,0,0,0.5));z-index:1;max-height:unset;width:2560px;min-width:2560px">
    </div>
</div>

<div class="snap"></div>

<div class="section" style="background-image: url('/assets/framed/svg/Topography.svg');height:100vh;background-size:cover;background-attachment:fixed;filter:drop-shadow(0px 0px 2px rgba(0,0,0,0.5))">
    <p class="framed viewer bottom-tab" style="font-size:18pt;background:#333;letter-spacing:0em">FRAMED</p>
    <a href="/framed/" style="width:576px;max-width:80%">
        <img src="/assets/framed/svg/FramedLogoLarge.svg" title="visit the site!" class="glow-hover">
    </a>  
</div>

<div class="snap"></div>

<style>
.bordered-grid {
    display: grid;
    grid-template-columns: 50% auto 50%;
    gap: 0;
    align-items: center;                 
    justify-items: center;
    width: 1200px;                         
    max-width: 80%;
    background: #f6f6f3;
    border-radius: 10pt;
    filter: drop-shadow(0px 0px 2px rgba(32, 16, 16, 0.25));
}

.grid-item {
    padding: 20px;
    text-align: center;
}

.grid-item.divider {
    padding:0;
    height:300px;
    width:1px;
    background-color:#cbc8c5
}

@media (max-width: 1200px) {
	.bordered-grid {
		grid-template-columns: 1fr;
		width:672px;
	}

    .grid-item.divider {
        height:1px;
        width:300px;
    }
}
</style>

<div class="section" style="background: linear-gradient(180deg, #f6f6f3 75%, #deddda 100%);filter:drop-shadow(0px 0px 2px rgba(0,0,0,0.5));scroll-snap-align:start;scroll-snap-stop:always;position:relative;top:unset">
    <p class="main-text bottom-tab" style="font-family:'DM Sans';font-weight:800;background:#f6f6f3">about me</p>
    <div class="bordered-grid" style="z-index:100;color:#201010">
        <div class="grid-item">
            <p style="text-align:left;margin:12pt">Hi! My name's Ian, creating online under the pseudonym <span style="font-family:'DM Sans';font-weight:700">moyevka</span>. I hope my work's spoken for itself! Outside of all this creative stuff, I'm a karaoke nuisance, cat owner (that's them on this page!), and a pretty alright home cook.</p>
            <hr>
            <h1>about this site</h1> 
            <p style="text-align:left;margin:12pt"> This site is written from scratch! Pure HTML, CSS and JS, with Jekyll for a modular authoring setup and to build the site, which is then hosted on Github Pages. No W*x, no S***resp*ce, no plugins at all. <br><br> A main goal for this website was to have each project's page be presented in a unique theme of its own, highlighting my understanding of the project's design goals and aesthetic. I like to think that I've accomplished that. <br><br> <i>By no means am I a web developer. I do not intend for this to be part of my jobscope.</i></p>
        </div>
        <div class="grid-item divider"></div>
        <div class="grid-item">
            <h1>contact</h1> 
            <p style="margin:12pt" class="site">
                <a href="https://x.com/moyevka" target="_blank" style="text-decoration:unset">
                    <img src="/assets/site/x-logo.svg" style="width:1em;vertical-align:sub"> @moyevka
                </a>
            </p>
        </div>
    </div>
    <div class="post-gallery" id="columnPlace-randomSort">
    {% assign images = site.static_files | where: "image", true | sort: "name" | reverse %}
    {% for image in images %}
        {% if image.path contains 'site/cats/' %}
            <div class="post-item randrot" style="border-radius:5pt">
                <img src="{{ image.path }}" alt="{{ image.name }}" class="movable clickable" style="border-radius:5pt">
            </div>
        {% endif %}
    {% endfor %}
    </div>
    <img src="/assets/splash/about-me.svg" style="max-height:unset;width:100vw;height:auto;position:absolute;bottom:0;z-index:-1">
</div>