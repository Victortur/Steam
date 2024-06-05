<template>
    <div>
        <TituloBuscador></TituloBuscador>
    </div>

    <section class="ordenNavComunidad1">
        <nav class="ordenNavComunidad">
            <ul class="navCenterComunidad">
                <li>
                    <NuxtLink to="/ComunidadPages/Inicio">Inicio</NuxtLink>
                </li>
                <li>
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Artworks">Artworks</NuxtLink>
                </li>
                <li>
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Mercado">Mercado</NuxtLink>
                </li>
                <li>
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Retransmisiones">Retransmisiones
                    </NuxtLink>
                </li>
            </ul>
        </nav>
    </section>

    <section>
        <h1 class="TituloInicioComunidad">Posts Recientes</h1>

        <section v-if="data != null">
            <ComunidadPostsIzq v-for="(game, index) in data.results.slice(0, numberOfPostsToShow)" :key="index"
                :game="game" :count="index" />
        </section>

        <button class="VerMas" @click="togglePosts">
            <p>{{ showMore ? 'Ver menos' : 'Ver más' }}</p>
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

            .textHover {
                transition: 300ms;

                &:hover {
                    color: #0047ff;
                }
            }
        }
    }
}

.TituloInicioComunidad {
    margin-top: 50px;
    padding: 0px 120px;
    font-size: larger;
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

let numberOfPostsToShow = ref(3);
const showMore = ref(false);

const togglePosts = () => {
    showMore.value = !showMore.value;
    numberOfPostsToShow.value = showMore.value ? 15 : 3;
};
</script>