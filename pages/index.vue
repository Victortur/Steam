import ArticleCard from '~/components/global/ArticleCard.vue';
<template>
    <div>
        <TituloHome></TituloHome>
        <HeaderImage :source="'/img1.jpg'"></HeaderImage>
    </div>

    <section class="ImgTienda">
        <CarruselHome></CarruselHome>
    </section>

    <section class="container cards-section">
        <ArticleCard
        v-for="(article, index) in articles"
        :key="index"
        :article="article">
        </ArticleCard>
    </section>
</template>

<script setup>
    import { ref } from 'vue'
    const title = ref('Página de inicio')

    const articles =ref([
    {
        id:1,
        title: "Artículo 1",
        url: "https://fastly.picsum.photos/id/113/1024/300.jpg?hmac=TOHUmfAAmudYJQi9qnvSB7rExXTt5fGNfU7s_cE7mlA"
    },
    {
        id:2,
        title: "Artículo 2",
        url: "https://fastly.picsum.photos/id/113/1024/300.jpg?hmac=TOHUmfAAmudYJQi9qnvSB7rExXTt5fGNfU7s_cE7mlA"
    },
    {
        id:3,
        title: "Artículo 3",
        url: "https://fastly.picsum.photos/id/113/1024/300.jpg?hmac=TOHUmfAAmudYJQi9qnvSB7rExXTt5fGNfU7s_cE7mlA"
    },
    {
        id:4,
        title: "Artículo 4",
        url: "https://fastly.picsum.photos/id/113/1024/300.jpg?hmac=TOHUmfAAmudYJQi9qnvSB7rExXTt5fGNfU7s_cE7mlA"
    }
    ])
</script>

<style lang="postcss">
    .cards-section{
        display: flex;
        justify-content: space-between;
    }
    .ImgTienda {
    width: 600px;
}
</style>