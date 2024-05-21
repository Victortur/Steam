<script setup lang="ts">
import TarjetaLargaJuego from '~/components/TarjetaLargaJuego.vue';
</script>

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
                    <NuxtLink to="/ComunidadPages/Artworks">Artworks</NuxtLink>
                </li>
                <li>
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Mercado">Mercado</NuxtLink>
                </li>
                <li>
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Retransmisiones">Retransmisiones</NuxtLink>
                </li>
            </ul>

        </nav>
    </section>

    <section>
        <h1 class="TituloArtworksComunidad">Más destacados</h1>
        <ArticleArtwork></ArticleArtwork>
        <h1 class="TituloArtworksComunidad">Según tus juegos</h1>
        <TarjetaLargaJuego></TarjetaLargaJuego>

    </section>
    

</template>

<style lang="postcss">
.ordenNavComunidad1{
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
        border-top: solid  0.5px white;
        border-bottom: solid  0.5px white;
        .NavComunidadGreyText{
            color: grey;
        }
    }
}
}

.TituloArtworksComunidad{
    margin-top: 50px;
    padding: 0px 120px;
    font-size: larger;
}

</style>