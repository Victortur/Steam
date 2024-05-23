<template>
    <div>
        <HeaderImage :source="'/img2.jpg'"></HeaderImage>
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
            <PastillaJuegos
                v-for="(game, index) in data.results.slice(0, numberOfGamesToShow)"
                :key="index"
                :game="game"
                :count="index"
            />
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
            <PastillaJuegos
                v-for="(game, index) in data.results.slice(0, numberOfGamesToShow2)"
                :key="index"
                :game="game"
                :count="index"
            />
        </section>
    </section>
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
        background-color:#0047ff;
    }
}
</style>

<script setup>
const { data } = useFetch('https://api.rawg.io/api/games?key=d45f1e8e88654d059e56f179e27d9327');

let numberOfGamesToShow = 1; // Define cuántos juegos quieres mostrar
let numberOfGamesToShow2 = 2; // Define cuántos juegos quieres mostrar

</script>