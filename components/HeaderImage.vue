<template>
    <div class="carousel">
        <div class="carousel-inner" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
            <div class="carousel-item">
                <NuxtLink ><img class="HeaderImg" src="public/gif1.gif" alt=""></NuxtLink>
                <div class="caption"><h2>Tienda</h2></div>
            </div>
            <div class="carousel-item">
                <NuxtLink to="/ComunidadPages/Inicio"><img class="HeaderImg" src="public/gif5.gif" alt=""></NuxtLink>
                <div class="caption"><h2>Comunidad</h2></div>
            </div>
            <div class="carousel-item">
                <NuxtLink to="/SteamCreate"><img class="HeaderImg" src="public/gif6.gif" alt=""></NuxtLink>
                <div class="caption"><h2>SteamCreate</h2></div>
            </div>
        </div>
        <button class="prev" @click="prevSlide">❮</button>
        <button class="next" @click="nextSlide">❯</button>
    </div>
</template>

<style lang="postcss">
.HeaderImg {
    margin-top: 60px;
    width: 100%;
    height: 500px;
    object-fit: cover;
}

.carousel {
    position: relative;
    overflow: hidden;
}

.carousel-inner {
    display: flex;
    transition: transform 0.5s ease;
}

.carousel-item {
    flex: 0 0 100%;
    position: relative;
}

.caption {
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    color: white;
    font-size: 20px;
}

.prev,
.next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 50px;
    height: 50px;
    background: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    cursor: pointer;
}

.prev {
    left: 10px;
}

.next {
    right: 10px;
}
</style>

<script setup>
import { ref } from 'vue';

const currentIndex = ref(0);
const totalSlides = 3;

function nextSlide() {
    currentIndex.value = (currentIndex.value + 1) % totalSlides;
}

function prevSlide() {
    currentIndex.value = (currentIndex.value - 1 + totalSlides) % totalSlides;
}
</script>