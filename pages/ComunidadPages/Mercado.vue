<template>
    <div>
        <TituloBuscador></TituloBuscador>
    </div>

    <section class="ordenNavComunidad1">
        <nav class="ordenNavComunidad">
            <ul class="navCenterComunidad">
                <li>
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Inicio">Inicio</NuxtLink>
                </li>
                <li>
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Artworks">Artworks</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/ComunidadPages/Mercado">Mercado</NuxtLink>
                </li>
                <li>
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Retransmisiones">Retransmisiones
                    </NuxtLink>
                </li>
            </ul>
        </nav>
    </section>

    <section>
        <nav class="NavMercado">
            <NuxtLink to="/ComunidadPages/Mercado">
                <h1 class="TituloInicioComunidad2">Articulos populares</h1>
            </NuxtLink>
            <NuxtLink to="/ComunidadPages/MercadoPages/MercadoRecientes">
                <h1 class="TituloInicioComunidad">Recientes</h1>
            </NuxtLink>
        </nav>

        <section v-if="data != null">
            <PastillaJuegos v-for="(game, index) in data.results.slice(0, numberOfGamesToShow)" :key="index"
                :game="game" :count="index" />
        </section>

        <button class="VerMas" @click="toggleGames">
            <p>
                {{ showMore ? 'Ver menos' : 'Ver más' }}
            </p>
        </button>
    </section>
</template>

<style lang="postcss">
.ordenNavComunidad1 {
    display: flex;
    justify-content: center;

    .ordenNavComunidad {
        padding: 10px 60px;
        font-size: 13px;
        width: 1000px;

        .navCenterComunidad {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
    }
}

.NavMercado {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    .TituloInicioComunidad2 {
        margin-top: 50px;
        padding: 0px 120px;
        font-size: larger;
        color: #0047ff;

        @media (max-width: 500px) {
            margin-top: 50px;
            padding: 0px 20px;
            font-size: 10px;
            color: #0047ff;
        }
    }
}

.VerMas {
    margin: 0px 120px;
    font-size: 13px;
    background-color: #0047ff;
    padding: 10px;
    border-radius: 10px;
    margin-bottom: 40px;
}
</style>

<script setup>
import { ref } from 'vue';
const { data } = useFetch('https://api.rawg.io/api/games?key=d45f1e8e88654d059e56f179e27d9327');

let numberOfGamesToShow = ref(6);
const showMore = ref(false);

const toggleGames = () => {
    showMore.value = !showMore.value;
    numberOfGamesToShow.value = showMore.value ? 25 : 6;
};
</script>