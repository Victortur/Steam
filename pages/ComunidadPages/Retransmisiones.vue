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
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Artworks">Artworks</NuxtLink>
                </li>
                <li>
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Mercado">Mercado</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/ComunidadPages/Retransmisiones">Retransmisiones</NuxtLink>
                </li>
            </ul>

        </nav>
    </section>

    <section>
        <h1 class="TituloArtworksComunidad">En directo ahora</h1>

        <div class="OrdenDirecto">
            <div class="OrdenDirecto2">
                <img src="public/illojuan.svg" alt="directoIlloJuan">

                <div class="DirectoInfo">
                    <div>
                        <img class="ImgStream" src="public/illo2Circulo.svg" alt="">
                    </div>
                    <div class="NombreStream">
                        <h5>Jugando a Red Dead Redemption!!</h5>
                        <h6>Illojuan</h6>

                    </div>
                </div>
            </div>
        </div>

        <Directos></Directos>
        <Directos></Directos>
        <Directos></Directos>



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
            border-top: solid 0.5px white;
            border-bottom: solid 0.5px white;

            .NavComunidadGreyText {
                color: grey;
            }
        }
    }
}

.TituloArtworksComunidad {
    margin-top: 50px;
    padding: 0px 120px;
    font-size: larger;
}

.OrdenDirecto {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: 40px;

    .OrdenDirecto2 {
        width: 1000px;
        display: flex;
        flex-direction: column;
        padding: 20px;
        border-radius: 40px;
        background-color: rgba(17, 18, 22, 1);
        .DirectoInfo {
            display: flex;
            flex-direction: row;
            margin-top: 20px;
            .ImgStream{
                width: 40px;
                display: flex;
                align-self: center;
            }
            .NombreStream{
                margin-left: 20px;
            }
        }
    }


}
</style>