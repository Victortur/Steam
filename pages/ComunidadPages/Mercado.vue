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
                    <NuxtLink class="NavComunidadGreyText" to="/ComunidadPages/Retransmisiones">Retransmisiones</NuxtLink>
                </li>
            </ul>

        </nav>
    </section>

</template>

<style lang="postcss">
.ordenNavComunidad1{
    display: flex;
    justify-content: center;
    .ordenNavComunidad {
    padding: 10px 60px;
    font-size: 13px;
    border-bottom: solid 0.5px white;
    width: 1000px;

    .navCenterComunidad {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}
}

</style>