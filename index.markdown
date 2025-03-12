---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<style>
    body {
        margin: 0;
        overflow: hidden;
        background: black;
        color: white;
        font-family: Arial, sans-serif;
    }
    .container {
        position: relative;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
    }
    .text {
        font-size: 15vw;
        font-weight: bold;
        text-align: center;
        background: url('/ceramics_two_photos/Ginkgo.jpg') no-repeat center center;
        background-size: cover;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        color: transparent;
        transition: font-size 0.5s ease;
        cursor: pointer;
    }
</style>

<script>
    window.addEventListener('scroll', function() {
        const textElement = document.querySelector('.text');
        const scrollPosition = window.scrollY;
        const newFontSize = 10 + scrollPosition / 10;
        textElement.style.fontSize = newFontSize + 'vw';
    });

    document.addEventListener('DOMContentLoaded', function() {
        document.querySelector('.text').addEventListener('click', function() {
            window.location.href = 'gallery';
        });
    });
</script>

<div class="container">
    <div class="text">Art by Gabo</div>
</div>
