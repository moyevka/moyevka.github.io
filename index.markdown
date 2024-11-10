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
        height:100svh;
        padding:0;
        position:sticky;
        top:0;
        max-width:100vw;
        overflow:visible;
        overflow-x:clip
    }

    .homeblock {
        max-width:500px
    }

    .moyevka {
        font-family:'PP Pangaia';
        font-size:96pt;
    }

    .moyevkaSub {
        font-style:italic;
        left:36pt;
        bottom:-8pt;
        position:relative;
        margin:0;
        font-size:20pt;
        letter-spacing:-0.05em
    }
    .framed.viewer {
        font-size: 18pt;
    }
    .card.tags {
        position:absolute;
        bottom:4rem;
        z-index:5
    }
    .card.contact {
        position:absolute;
        bottom:20vh;
    }
@media (max-height:1080px) {
    .card.contact {
        bottom: 4rem;
        right: 4rem
    }
}
@media (min-resolution: 144dpi) and (max-aspect-ratio: 1/1) {
    .snap {
        scroll-snap-align:none;
        scroll-snap-stop:normal;
    }
    .homeblock{
        max-width:600px;
        margin-left:4vh;
        margin-right:4vh;
    }
    .moyevka {
        font-size:114pt;
    }
    .moyevkaSub {
        left:27pt;
        bottom:-8pt;
        font-size:32pt;
    }
    .bottom-tab {
        font-size: 2rem;
        top: -64pt;
        padding-bottom: 22pt
    }
    .framed.viewer {
        font-size: 2rem;
    }
    .card.tags {
        bottom: 10vh;
    }
    .card.contact {
        bottom: 10vh;
    }
}
</style>

<div class="snap"></div>

<div class="section" style="background: linear-gradient(180deg, #f6f6f3 75%, #deddda 100%)">
    <div class="homeblock" style="text-align:left;color:#201010">
        <p class="moyevkaSub"><i>oh hey! it's</i></p>
        <p class="moyevka" style="margin:0;line-height:0.6;letter-spacing:-0.05em">moyevka!</p>
        <br>
        <p>visual artist, graphic designer, whatever you wanna call it, i just like to make stuff that looks cool. <br> let's create something together!</p>
    </div>
    <div class="card contact">
        <p style="margin:12pt;text-align:left" class="site">
            get in touch: <br>
            <a href="mailto:contact@moyevka.work" target="_blank" style="font-family:'DM Sans';font-weight:800;text-decoration:unset">
                <img src="/assets/site/logo-mail.svg" style="width:1.25em;vertical-align:text-bottom;margin-right:0.25rem"> contact@moyevka.work
            </a>
        </p>
    </div>
    <img src="/assets/splash/home-bottom.svg" class="homebg" style="width:auto;height:auto;position:absolute;bottom:0;left:0;z-index:-1">
    <img src="/assets/splash/home-top.svg" class="homebg" style="width:auto;height:auto;position:absolute;top:0;right:0;z-index:-1">
</div>

<div class="snap"></div>

<div class="section" style="background-image: url('/assets/splash/naps-splash.png'); background-color:white; min-height:100svh; background-repeat: no-repeat; background-position: center; background-size: auto 1325px; image-rendering: pixelated;filter:drop-shadow(0px 0px 2px rgba(32, 16, 16, 0.5))" id="napsbg">
    <p class="main-text bottom-tab"><i>scroll down to see my work!</i></p>
    <p><a href="/naps/" class="naps-title main outlined">naps!</a></p>
    <div class="card tags">
        <p style="font-family:'DM Sans';font-weight:800;margin:0" class="site">personal | illustrative design, digital</p>
    </div>  
</div>

<script>
    const napsBg = document.getElementById('napsbg');
    
    if (napsBg) {
        const scaleFactor = window.devicePixelRatio;
        
        if (scaleFactor !== 1) {
            let bgSize;
            if (scaleFactor >= 2) {
                // For devicePixelRatio 2 and above
                bgSize = `unset`;
                napsBg.style.imageRendering = `auto`;
            } else {
                // For devicePixelRatio between 1 and 2
                bgSize = `auto ${(1 / scaleFactor) * 1325}px`;
            }
            napsBg.style.backgroundSize = bgSize;
        } else {
            // Reset background-size if devicePixelRatio is 1
            napsBg.style.removeProperty('background-size');
        }
    }
</script>

<div class="snap"></div>

<div class="section" style="background:radial-gradient(ellipse at bottom, #fccc85 0%, #fc9800 100%);filter:drop-shadow(0px 0px 2px rgba(0,0,0,0.5))">
    <p class="carle white-text bottom-tab" style="margin:0;font-weight:800;background:#fc9800;letter-spacing:0em;text-shadow: 1px 1px 2px rgba(0,0,0,0.5);">CARLE</p>
    <a href="/carle/" class="carle title white-text" style="z-index:2">
        <img src="/assets/carle/svg/carle-logo-stack.svg" class="carle-logo hover">
    </a> 
    <div style="position:absolute;height:100%;width:100%;overflow:clip;display:flex;justify-content:center;align-items:center">
        <img src="/assets/carle/svg/paint-2.svg" style="filter:drop-shadow(2px 2px 4px rgba(0,0,0,0.5));z-index:1;max-height:unset;width:2560px;min-width:2560px">
    </div>
    <div class="card tags">
        <p style="font-family:'DM Sans';font-weight:800;margin:0" class="site">commercial | design & advertising, photovideo</p>
    </div>  
</div>

<div class="snap"></div>

<div class="section" style="background: url('/assets/framed/svg/Topography.svg'), #333;height:100svh;background-size:cover;background-attachment:fixed;filter:drop-shadow(0px 0px 2px rgba(0,0,0,0.5))">
    <p class="framed viewer bottom-tab" style="background:#333;letter-spacing:0em">FRAMED</p>
    <a href="/framed/" style="width:576px;max-width:80%">
        <img src="/assets/framed/svg/FramedLogoLarge.svg" title="visit the site!" class="glow-hover">
    </a>
    <div class="card tags">
        <p style="font-family:'DM Sans';font-weight:800;margin:0" class="site">freelance | design & branding, digital</p>
    </div>  
</div>

<div class="snap"></div>

<style>
.bordered-grid {
    display: grid;
    grid-template-columns: 50% auto 50%;
    gap: 0;
    align-items: center;                 
    justify-items: center;
    max-width: 1200px;                         
    margin: 4vh;
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
	}

    .grid-item.divider {
        height:1px;
        width:300px;
    }
}
</style>

<div class="section" style="background: linear-gradient(180deg, #f6f6f3 75%, #deddda 100%);filter:drop-shadow(0px 0px 2px rgba(0,0,0,0.5));position:relative;top:unset;height:auto;padding-top:2rem;padding-bottom:2rem">
    <p class="main-text bottom-tab" style="font-family:'DM Sans';font-weight:800;background:#f6f6f3">about me</p>
    <div class="bordered-grid" style="z-index:100;color:#201010">
        <div class="grid-item">
            <p style="text-align:left;margin:12pt">Hi! My name's Ian, creating online under the pseudonym <span style="font-family:'DM Sans';font-weight:700">moyevka</span>. I hope my work's spoken for itself! If not, I'm a designer, artist, video editor, photographer, so on. I work well in Illustrator, Clip Studio Paint, Photoshop, Lightroom, Premiere Pro, After Effects, Blender, Nuke, and more. Outside of all this creative stuff, I'm a karaoke nuisance, cat owner (that's them on this page!), and a pretty alright home cook.</p>
            <hr>
            <h1>about this site</h1> 
            <p style="text-align:left;margin:12pt"> This site is written from scratch! Pure HTML, CSS and JS, with Jekyll for a modular authoring setup and to build the site, which is then hosted on Github Pages. No w*x, no sq**r*sp*c*, no plugins for anything. <br><br> A main goal for this website was to have each project's page be presented in a unique theme of its own, highlighting my understanding of the project's design goals and aesthetic. I like to think that I've accomplished that. <br><br> <i>I am not a trained web developer. Please don't ask me to make your website.</i></p>
        </div>
        <div class="grid-item divider"></div>
        <div class="grid-item">
            <h1>find me here:</h1> 
            <p style="margin:12pt;text-align:left;line-height:2" class="site">
                <a href="mailto:contact@moyevka.work" target="_blank" style="font-family:'DM Sans';font-weight:800;text-decoration:unset">
                    <img src="/assets/site/logo-mail.svg" style="width:1.25em;vertical-align:text-bottom;margin-right:0.5rem"> contact@moyevka.work
                </a>
                <br>
                <a class="logotrans" href="https://x.com/moyevka" target="_blank" style="font-family:'DM Sans';font-weight:800;text-decoration:unset">
                    <img class="logo-x" src="/assets/site/logo-x.svg" style="width:1.25em;vertical-align:text-bottom;margin-right:0.5rem">
                    <img class="logo-twitter" src="/assets/site/logo-twitter.svg" style="width:1.25em;vertical-align:text-bottom;margin-right:0.5rem"> 
                    <span style="left:-2.25rem;position:relative">@moyevka</span>
                </a>
                <br>
                <a href="https://bsky.app/profile/moyevka.bsky.social" target="_blank" style="font-family:'DM Sans';font-weight:800;text-decoration:unset">
                    <img src="/assets/site/logo-bsky.svg" style="width:1.25em;vertical-align:text-bottom;margin-right:0.5rem"> @moyevka.bsky.social
                </a>
            </p>
        </div>
    </div>
    <div class="post-gallery" id="columnPlace-randomSort" style="overflow:clip">
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

<div class="snap"></div>