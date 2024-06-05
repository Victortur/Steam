import ArticleCard from '~/components/global/ArticleCard.vue';
<template>
    <div>
        <HeaderImage></HeaderImage>
        <TituloHome></TituloHome>
    </div>

    <div class="ApartadoLinea">
        <div>
            <h4>Próximamente</h4>
        </div>
        <div class="Linea"></div>
    </div>
    <section>
        <section v-if="data != null">
            <PastillaInfo v-for="(game, index) in data.results.slice(0, numberOfGamesToShow)" :key="index" :game="game"
                :count="index" />
        </section>
    </section>

    <div class="ApartadoLinea">
        <div>
            <h4>Hoy</h4>
        </div>
        <div class="Linea"></div>
    </div>




    <section>
        <section v-if="data != null">
            <PastillaInfo v-for="(game, index) in data.results.slice(0, numberOfGamesToShow2)" :key="index" :game="game"
                :count="index" />
            <PastillaJuegos v-for="(game, index) in data.results.slice(0, numberOfGamesToShow2)" :key="index"
                :game="game" :count="index" />
        </section>
    </section>

    <div class="Linea1"></div>

    <section class="OrdenServicios">
        <h2 class="OrdenServicios1">Otros servicios</h2>
    </section>

    <Servicios></Servicios>
    <Servicios2></Servicios2>


</template>

<style lang="postcss">
.ApartadoLinea {
    margin: 0px 120px;
    display: flex;
    flex-direction: row;
    align-items: center;

    .Linea {
        width: 100%;
        height: 1px;
        margin-left: 40px;
        background-color: #0047ff;
    }
}

.Linea1 {
    width: 100%;
    height: 1px;
    background-color: #0047ff;
}
.OrdenServicios{
    margin: 40px 120px;
    @media (max-width: 500px) {
        margin: 20px 20px;
        
        }
    .OrdenServicios1{
        @media (max-width: 500px) {
            font-size: 20px;
        }


    }
}
</style>

<script setup>

const { data } = useFetch('https://api.rawg.io/api/games?key=ed55e0ad388f4039b1f1f7b96d735708');

let numberOfGamesToShow = 1; // Define cuántos juegos quieres mostrar
let numberOfGamesToShow2 = 2; // Define cuántos juegos quieres mostrar




import { ref } from 'vue'
const title = ref('Página de inicio')

const articles = ref([
    {
        id: 1,
        title: "Artículo 1",
        url: "https://fastly.picsum.photos/id/113/1024/300.jpg?hmac=TOHUmfAAmudYJQi9qnvSB7rExXTt5fGNfU7s_cE7mlA"
    },
    {
        id: 2,
        title: "Artículo 2",
        url: "https://fastly.picsum.photos/id/113/1024/300.jpg?hmac=TOHUmfAAmudYJQi9qnvSB7rExXTt5fGNfU7s_cE7mlA"
    },
    {
        id: 3,
        title: "Artículo 3",
        url: "https://fastly.picsum.photos/id/113/1024/300.jpg?hmac=TOHUmfAAmudYJQi9qnvSB7rExXTt5fGNfU7s_cE7mlA"
    },
    {
        id: 4,
        title: "Artículo 4",
        url: "https://fastly.picsum.photos/id/113/1024/300.jpg?hmac=TOHUmfAAmudYJQi9qnvSB7rExXTt5fGNfU7s_cE7mlA"
    }
])
</script>