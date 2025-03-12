---
layout: default
title: Gallery
permalink: /gallery/
---

<div class="gallery">
    <div class="gallery-item"><img src="/ceramics_two_photos/Bulb_cups.jpg" alt="Bulb cups" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/assets/images/Ceramics/Black_white_set.JPG" alt="Black and white set" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Chatter_bowls.jpg" alt="Chatter bowls" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Chatter_bowls_green.jpg" alt="Green chatter bowls" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Crack_vase.jpg" alt="Crack vase" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Crackle_set.jpg" alt="Crackle set" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Four_bowl_set.jpg" alt="Four bowl set" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Horse_bowls.jpg" alt="Horse bowls" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Liv_bowl.jpg" alt="Liv bowl" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Rusty_cups.jpg" alt="Rusty cups" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Sand_set.jpg" alt="Sand set" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Smooth_bowl.jpg" alt="Smooth bowl" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Ugly_set.jpg" alt="Ugly set" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Brides_cups.jpg" alt="Brides cups" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/assets/images/Ceramics/Na_cup.JPG" alt="Na cup" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/assets/images/Ceramics/Tall_bowls.JPG" alt="Tall bowls" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/assets/images/Ceramics/Brown_bowl.JPG" alt="Brown bowl" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/assets/images/Ceramics/Chatter_cup.JPG" alt="Chatter cup" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/assets/images/Ceramics/Flower_plate.JPG" alt="Flower plate" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/assets/images/Ceramics/Horse_vase.JPG" alt="Horse vase" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/assets/images/Ceramics/Tea_pot.JPG" alt="Tea pot" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/assets/images/Ceramics/Texture_bowl.JPG" alt="Texture bowl" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/assets/images/Ceramics/Twovase2.JPG" alt="Two vases" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Chatter_cup_green.jpeg" alt="Chatter cup" style="object-fit: cover; width: 100%; height: 100%;"></div>
    <div class="gallery-item"><img src="/ceramics_two_photos/Ginkgo.jpg" alt="Chatter cup" style="object-fit: cover; width: 100%; height: 100%;"></div>
</div>

<style>
.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 5px;
}
.gallery-item {
    box-sizing: border-box;
    transition: transform 0.3s ease-in-out;
}
.gallery-item img {
    width: 100%;
    height: auto;
    display: block;
    cursor: pointer;
}
.gallery-item:hover {
    transform: scale(1.05);
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const galleryItems = document.querySelectorAll('.gallery-item img');
    galleryItems.forEach(item => {
        item.addEventListener('click', function() {
            const overlay = document.createElement('div');
            overlay.classList.add('overlay');
            const img = document.createElement('img');
            img.src = this.src;
            img.classList.add('overlay-img');
            const closeButton = document.createElement('span');
            closeButton.classList.add('close-button');
            closeButton.innerHTML = '&times;';
            closeButton.addEventListener('click', function() {
                document.body.removeChild(overlay);
            });
            overlay.appendChild(img);
            overlay.appendChild(closeButton);
            document.body.appendChild(overlay);
        });
    });
});
</script>

<style>
.overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.8);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
}
.overlay-img {
    max-width: 90%;
    max-height: 90%;
}
.close-button {
    position: absolute;
    top: 20px;
    right: 20px;
    font-size: 40px;
    color: white;
    cursor: pointer;
}
</style>
