---
title: 02 naps
layout: naps
tags: illustration, design
---

<div class="container">
    <div class="container-item" style="align-items:center;flex-flow:row">
        <div id="stickerGallery" class="navbuttons" style="position:relative;top:unset;left:unset;margin:1rem">
            <div class="button naps roundicon" id="previousItem" title="previous" style="padding:0.33rem;border-radius:0.33rem">
                <img src="/assets/site/up.svg">
            </div>
            <div class="button naps roundicon" id="nextItem" title="next" style="padding:0.33rem;border-radius:0.33rem">
                <img src="/assets/site/down.svg">
            </div>
        </div>
        <div class="image-gallery" id="stickerGallery">
            {% assign images = site.static_files | where: "image", true | sort: "name" | reverse %}
            {% for image in images %}
                {% if image.path contains 'naps/stickers/' %}
                    <div class="gallery-item">
                        <img src="{{ image.path }}" alt="{{ image.name }}" class="clickable naps-img">
                    </div>
                {% endif %}
            {% endfor %}
        </div>
    </div>
    <div class="container-item header" style="z-index:2;background:white;padding:48px">
        <p class="naps-title">stickers</p>
        <p class="binary" style="max-width:480px">made in under a weekend each, these 'stickers' are the ground zero for the naps project. a combination of illustration, design & typography packaged in 1-bit 512x512 images, they were born from experiments with a low fidelity artstyle that could be done quickly and still presented as punchy and distinct. i started to really lean into these during my time in national service, where i was only afforded a weekend of free time to pursue my hobbies. <br><br> made in clip studio paint, illustrator</p>
    </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const galleries = document.querySelectorAll('.navbuttons');

    galleries.forEach(nav => {
        const navId = nav.id;
        const gallery = document.querySelector(`.image-gallery[id="${navId}"]`);
        if (!gallery) return;

        const prevBtn = nav.querySelector(`#previousItem${navId.replace('stickerGallery', '')}`);
        const nextBtn = nav.querySelector(`#nextItem${navId.replace('stickerGallery', '')}`);

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

            if (currentIndex === totalItems - 3) {
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

