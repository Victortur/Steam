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
                <h1 class="TituloInicioComunidad">Articulos populares</h1>
            </NuxtLink>

            <NuxtLink to="/ComunidadPages/MercadoPages/MercadoRecientes">
                <h1 class="TituloInicioComunidad2">Recientes</h1>
            </NuxtLink>

        </nav>

        <PastillaJuegos></PastillaJuegos>
        <PastillaJuegos></PastillaJuegos>
        <PastillaJuegos></PastillaJuegos>

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
    }
}
</style>
