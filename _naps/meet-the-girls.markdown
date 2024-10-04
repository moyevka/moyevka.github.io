---
layout: naps
title: 01 naps
tags: illustration, design
---

<style>
    .mtgtitle {
        font-style:normal;
        line-height:1;
        font-size:56pt;
        margin:0;
        margin-bottom:18px
    }
@media (min-resolution: 144dpi) and (max-aspect-ratio: 1/1) {
    .mtgtitle {
        font-size: 6rem;
        margin-bottom: 5rem
    }
    .item-title.naps-title {
        font-size: 5rem;
    }
}
</style>

<div class="g-container">
    <div class="g-item header">
        <p class="naps-title outlined mtgtitle">meet the girls!</p>
        <p class="binary outlined">get to know Mara, Sorrel, Choux, and Keys, the 4 girls of the naps project, through these highly stylised stylesheets - summarising the design and personality of each of them. <br><br> these stylesheets were created with the goal of exploring each character's personality, through the way they dress, to the colours they prefer. this is where i really leaned into the dithered almost pixelated-halftone look of naps, with a limited colour palette used across the sheets to unify them together. individual identity was given through colour and background choice, with each character's key colour being paired with its complement, and distinct textures used to curate the aesthetic of each girl. <br><br> made in clip studio paint, illustrator</p>
        <div id="mtgGallery" class="navbuttons" style="position:relative;left:unset;flex-flow:row">
            <div class="button naps roundicon" id="previousItem" title="previous" style="padding:0.33rem;border-radius:0.33rem">
                <img src="/assets/site/up.svg">
            </div>
            <div class="button naps roundicon" id="nextItem" title="next" style="padding:0.33rem;border-radius:0.33rem">
                <img src="/assets/site/down.svg">
            </div>
        </div>
    </div>
    <div class="g-item" style="flex-flow:row">
        <div class="g-gallery" id="mtgGallery">
            <div class="g-gallery-item" id="mainScroller">
                <img src="/assets/naps/meet-the-girls/CharSheet-1-Mara.png" alt="CharSheet-1-Mara" class="clickable naps-img">
                <div class="gallery-text">
                    <span class="item-title naps-title outlined"><span style="color:#f96b75">Mara</span> Saiph</span>
                    <span class="item-subtitle binary outlined">a little bit of a ditz with a tendency to fixate, she's somehow equal parts insecure and carefree</span>
                </div>
            </div>
            <div class="g-gallery-item">
                <img src="/assets/naps/meet-the-girls/CharSheet-2-Sorrel.png" alt="CharSheet-2-Sorrel" class="clickable naps-img">
                <div class="gallery-text">
                    <span class="item-title naps-title outlined"><span style="color:#364165">Sorrel</span> Hu</span>
                    <span class="item-subtitle binary outlined">catgirl with a capital C, she's as fierce as she is loyal, and one hell of a great friend. just don't annoy her.</span>
                </div>
            </div>
            <div class="g-gallery-item">
                <img src="/assets/naps/meet-the-girls/CharSheet-3-Choux.png" alt="CharSheet-3-Choux" class="clickable naps-img">
                <div class="gallery-text">
                    <span class="item-title naps-title outlined">Elodie "<span style="color:#7e9627">Choux</span>" Blythe</span>
                    <span class="item-subtitle binary outlined">aloof, moody & quiet - you'd think she'd be quite judgmental, but she's surprisingly sweet underneath all that</span>
                </div>
            </div>
            <div class="g-gallery-item">
                <img src="/assets/naps/meet-the-girls/CharSheet-4-Keys.png" alt="CharSheet-4-Keys" class="clickable naps-img">
                <div class="gallery-text">
                    <span class="item-title naps-title outlined">Kishori "<span style="color:#f07d2c">Keys</span>" Bhasin</span>
                    <span class="item-subtitle binary outlined">some may say she's a little too silly for her own good, but there's never a dull moment with her around</span>
                </div>
            </div>
        </div>
    </div>
</div>
<div class="bg-gallery" id="backgroundScroller" style="width:100%;position:absolute;top:0;margin:0;z-index:-1">
    <div class="bg-gallery-item" style="padding:0;height:100svh;position:relative">
        <img src="/assets/naps/meet-the-girls/mara-backdrop.png" style="width:auto;height:auto;position:absolute;bottom:-96px;left:0;image-rendering:pixelated">
    </div>
    <div class="bg-gallery-item" style="padding:0;height:100svh;position:relative">
        <img src="/assets/naps/meet-the-girls/sorrel-backdrop.png" style="width:auto;height:auto;position:absolute;bottom:-96px;left:0;image-rendering:pixelated">
    </div>
    <div class="bg-gallery-item" style="padding:0;height:100svh;position:relative">
        <img src="/assets/naps/meet-the-girls/choux-backdrop.png" style="width:auto;height:auto;position:absolute;bottom:-96px;left:0;image-rendering:pixelated">
    </div>
    <div class="bg-gallery-item" style="padding:0;height:100svh;position:relative">
        <img src="/assets/naps/meet-the-girls/keys-backdrop.png" style="width:auto;height:auto;position:absolute;bottom:0;left:0;image-rendering:pixelated">
    </div>
</div>

<script>
const gallery = document.querySelector('.g-gallery');
const firstItem = document.getElementById("mainScroller");
const backgroundScroller = document.getElementById("backgroundScroller");
backgroundScroller.style.backfaceVisibility = `hidden`;
gallery.addEventListener('scroll', () => {
    const topPosition = firstItem.getBoundingClientRect().top;
    backgroundScroller.style.transform = `translate3d(0, ${topPosition}px, 0)`;
});

document.addEventListener('DOMContentLoaded', function() {
    const galleries = document.querySelectorAll('.navbuttons');

    galleries.forEach(nav => {
        const navId = nav.id;
        const gallery = document.querySelector(`.g-gallery[id="${navId}"]`);
        if (!gallery) return;

        const prevBtn = nav.querySelector(`#previousItem${navId.replace('mtgGallery', '')}`);
        const nextBtn = nav.querySelector(`#nextItem${navId.replace('mtgGallery', '')}`);

        function getCurrentItemIndex() {
            const items = Array.from(gallery.children);
            let closestIndex = 0;
            let closestDistance = Infinity;
            items.forEach((item, index) => {
                const itemTop = item.offsetTop;
                const distance = Math.abs(gallery.scrollTop - itemTop);
                if (distance < closestDistance) {
                    closestDistance = distance;
                    closestIndex = index;
                }
            });
            return closestIndex;
        }

        function scrollToItem(index) {
            const items = gallery.children;
            const targetItem = items[index];
            if (targetItem) {
                gallery.scrollTo({
                    top: targetItem.offsetTop,
                    behavior: 'smooth'
                });
                updateButtonVisibility(index, items.length);
            }
        }

        function updateButtonVisibility(currentIndex, totalItems) {
            if (currentIndex === 0) {
                prevBtn.style.visibility = 'hidden';
            } else {
                prevBtn.style.visibility = 'visible';
            }

            if (currentIndex === totalItems - 1) {
                nextBtn.style.visibility = 'hidden';
            } else {
                nextBtn.style.visibility = 'visible';
            }
        }

        prevBtn.addEventListener('click', function() {
            const currentIndex = getCurrentItemIndex();
            if (currentIndex > 0) {
                scrollToItem(currentIndex - 1);
            }
        });

        nextBtn.addEventListener('click', function() {
            const currentIndex = getCurrentItemIndex();
            if (currentIndex < gallery.children.length - 1) {
                scrollToItem(currentIndex + 1);
            }
        });

        let isScrolling;
        gallery.addEventListener('scroll', function() {
            window.clearTimeout(isScrolling);
            isScrolling = setTimeout(function() {
                const currentIndex = getCurrentItemIndex();
                updateButtonVisibility(currentIndex, gallery.children.length);
            }, 100);
        });

        const initialIndex = getCurrentItemIndex();
        updateButtonVisibility(initialIndex, gallery.children.length);
    });
});
</script>