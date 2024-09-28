---
title: 02 framed
layout: framed
tags: design
---

<div class="wide-content fcard" style="z-index:1000">
    <div class="container" style="width:100%;gap:18pt">
        <div class="container-item" style="justify-content:start">
            <p class="framed subtitle" style="align-self:flex-start;margin:18pt">SITE OVERHAUL</p>
            <p class="framed">Following the recap above, I was tasked with retheming the <a href="https://framedsc.com/" target="_blank">framedsc.com</a> site to be in-line with the style developed for the recap. Due to the site's nature as documentation / a "wiki", my goal was focused on legibility over all else. One of the core decisions was the fonts used on the site. The site's body font (also used here) is <strong>Atkinson Hyperlegible</strong>, a font developed with readability in mind. <br><br> Colour choice was primarily an expansion of the existing FRAMED colours, #333333 and <span style="color:#333;background:#dcdfd8">#dcdfd8</span>, with intermediate shades of <span style="background:#272727">#272727</span> and <span style="color:#fff;background:#8A8A8A">#8A8A8A</span> forming a gradient of greys for use in darker backgrounds and secondary elements. A <span style="color:#56B6FB" title="color: #56B6FB">FRAMED Blue</span> was also developed to make elements of importance stand out against the monotone brand colours, with particular emphasis on the colour's contrast and saturation. Other coloured elements of the site like <a href="https://framedsc.com/contribute.htm#alert-boxes" target="_blank">alert boxes</a> were given subtle gradients based on their original colour, giving them more emphasis and dimension against the background.</p>
            <div class="slider" style="aspect-ratio: 1/1">
                <div class="slider__img slider__img-after">
                    <p>after</p>
                    <img src="/assets/framed/overhaul/headers-after.jpg" style="max-height:unset"/>
                </div>
                <div class="slider__img slider__img-before">
                    <p>before</p>
                    <img src="/assets/framed/overhaul/headers-before.jpg" style="max-height:unset" />
                </div>
                <input type="range" min="0" max="100" value="50" step="0.01" 
                    id="slider" class="slider__input" 
                    autocomplete="off" onwheel="this.blur()" 
            />
            </div>
            <p class="framed" style="margin-top:18pt">Part of this project also included remaking 125 existing headers to conform with the new site theme. Since these are static images, this involved sourcing the original screenshots without text and the blur border. In many cases, screenshots were replaced with more fitting compositions for the 1:5 aspect ratio. Since the author of the guide typically made the header as well, I ensured that screenshots replacing the originals came from the same author too. <br><br> I then put together a downloadable package to provide future authors with a Photoshop template and required assets to make these headers for their own contributions.</p>
        </div>
        <div class="container-item">
            <div class="slider" style="aspect-ratio: 1/2">
            <div class="slider__img slider__img-after">
                <p>after</p>
                <img src="/assets/framed/overhaul/site-after.jpg" style="max-height:unset"/>
            </div>
            <div class="slider__img slider__img-before">
                <p>before</p>
                <img src="/assets/framed/overhaul/site-before.jpg" style="max-height:unset" />
            </div>
            <input type="range" min="0" max="100" value="50" step="0.01" 
                id="slider" class="slider__input" 
                autocomplete="off" onwheel="this.blur()" 
            />
            </div>
        </div>
    </div>
</div>

<script>
    /**
 * Sliders should query all slider components on a page so we can have more than one on a page.
 */
 const sliders = Array.prototype.slice.call(
	document.querySelectorAll(".slider"),
  );
  
  /**
   * For each slider component we find, add an oninput event listener where we take the input value,
   * and set it to the polygon clip path of the before image for masking everything outside those dimensions.
   */
  sliders.forEach((slider) => {
	/* create divider */
	divider = document.createElement("DIV");
	divider.setAttribute("class", "slider__divider");
	/* place divider */
	slider.querySelector(".slider__img-after",).appendChild(divider);
	/* query slideValue */
	slider.querySelector(".slider__input").oninput = (e) => {
	  let slideValue = "calc(" + e.target.value + "% - 1px)";
	  /* set slideValue to clipPath */
	  slider.querySelector(
		".slider__img-before",
	  ).style.clipPath = `polygon(0 0,${slideValue} 0,${slideValue} 100%, 0 100%)`;
	  /* move divider based on slideValue */
	  slider.querySelector(
		".slider__divider",
	  ).style.left = "calc(" + e.target.value + "% - 1px)";
	};
  })
</script>