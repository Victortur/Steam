<template>

    <section v-if="data != null" class="SectDetalle">
        <div class="Ordendetalle">
            <div>
                <img src="public/DetCom.svg" alt="">
            </div>
            <div class="OrdenDetInfor">
                <h2>{{ data.name }}</h2>
                <h6 class="white">{{ data.description }}</h6>
            </div>
        </div>

    </section>


    <div class="carousel1">
        <div class="carousel-inner1" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
            <div class="carousel-item1">
                <NuxtLink><img class="HeaderImg1" src="public/scro1.svg" alt=""></NuxtLink>
            </div>
            <div class="carousel-item1">
                <NuxtLink><img class="HeaderImg1" src="public/scro2.svg" alt=""></NuxtLink>
            </div>
            <div class="carousel-item1">
                <NuxtLink><img class="HeaderImg1" src="public/scro3.svg" alt=""></NuxtLink>
            </div>
        </div>
        <button class="prev1" @click="prevSlide">❮</button>
        <button class="next1" @click="nextSlide">❯</button>
    </div>
</template>

<script setup>

const route = useRoute();
const { data } = useFetch(`https://api.rawg.io/api/games/${route.params.id}?key=ed55e0ad388f4039b1f1f7b96d735708`)

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

<style lang="postcss">
.SectDetalle {
    margin: 80px 0px;

    .Ordendetalle {
        display: flex;
        flex-direction: row;

        .OrdenDetInfor {
            display: flex;
            flex-direction: column;
            width: 40%;
            padding: 0px 20px;

            .white {
                color: white;
            }
        }
    }
}

.HeaderImg1 {
    width: 100%;
    height: 500px;
    object-fit: cover;
}

.carousel1 {
    position: relative;
    overflow: hidden;
    margin-bottom: 60px;
}

.carousel-inner1 {
    display: flex;
    transition: transform 0.5s ease;
}

.carousel-item1 {
    flex: 0 0 100%;
    position: relative;
}

.caption1 {
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    color: white;
    font-size: 20px;
}

.prev1,
.next1 {
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

.prev1 {
    left: 10px;
}

.next1 {
    right: 10px;
}
</style>