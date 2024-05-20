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
            <h1 class="TituloInicioComunidad">Articulos populares</h1>
            <h1 class="TituloInicioComunidad">Recientes</h1>
        </nav>

        <article class="ArticuloPastilla">
            <img src="public/PastillaJuego.svg" alt="">
            <div>
                <div>
                    <h4>Black Ops 4</h4>
                    <h6>Call of Duty</h6>
                </div>
                <div></div>
            </div>
        </article>

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
}

.ArticuloPastilla {}
</style>