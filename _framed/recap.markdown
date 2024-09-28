---
title: 01 framed
layout: framed
tags: design, data visualisation
---

<style>
    .recap-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        aspect-ratio: 16 / 9;
        width: 100%;
        max-width: 1440px;
        gap: 10px;
    }

    .recap-grid > * {
        box-shadow: 0px 0px 5px rgba(0,0,0,0.75);
        z-index: 1;
        transition: all 0.1s ease;
    }

    .recap-grid > *:hover {
        scale:102%;
        box-shadow: 0px 0px 10px rgba(0,0,0,0.5);
        z-index: 10;
        border-radius: 10pt;
    }

    .recap-grid .image-1 {
        grid-column: 1 / 2;
        grid-row: 1 / 3;
        aspect-ratio: 8 / 9;
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-top-left-radius: 10pt;
        border-bottom-left-radius: 10pt;
    }

    .recap-grid .image-2 {
        grid-column: 2 / 3;
        grid-row: 1 / 2;
        aspect-ratio: 16 / 9;
        width: 100%;
        object-fit: cover;
        border-top-right-radius: 10pt;
    }

    .recap-grid .image-3 {
        grid-column: 2 / 3;
        grid-row: 2 / 3;
        aspect-ratio: 16 / 9;
        width: 100%;
        object-fit: cover;
        border-bottom-right-radius: 10pt;
    }
</style>

<div class="wide-content fcard" style="padding-bottom:0">
<p class="framed title" style="margin-bottom:0">A YEAR OF FRAMED</p>
<hr>
<p class="framed subtitle">A RECAP OF THE YEAR 2021</p>
<div class="recap-grid">
  <img src="/assets/framed/recap/Recap-1.jpg" class="image-1 clickable framed-img" alt="Main Recap">
  <img src="/assets/framed/recap/Recap-2.jpg" class="image-2 clickable framed-img" alt="Timeline">
  <img src="/assets/framed/recap/Recap-3.jpg" class="image-3 clickable framed-img" alt="Stats">
</div>
<hr>
<p class="framed" style="max-width: 100%;text-align:left;margin:18pt;margin-top:0">A comprehensive data visualisation of the FRAMED Discord server's activity across the year 2021. This is where I started to develop the core of FRAMED's current aesthetic, introducing the drop-shadowed infocard look. Data was collated by other members while I processed the data using Google Sheets and designed everything in Illustrator. Aesthetically, design elements were inspired by existing graphics, made by older members, that used the same fonts and colours. This also marked the first appearance of the topography background, chosen to fit the FRAMED spirit of exploring (virtual) worlds. Since these posts were designed for social media (Twitter, currently X, specifically), the 8:9 / 16:9 / 16:9 aspect ratios of each post ensured that all elements were visible in the <a href="https://twitter.com/FramedSc/status/1477728223265914883" target="_blank">posted tweet.</a> <br><br> <i>I was unable to produce graphs for 2022 and 2023 due to National Service commitments.</i></p>
</div>