<template>
    <div>
        <TituloBuscador></TituloBuscador>
    </div>

    <section class="ordenNavComunidad1">
        <nav class="ordenNavComunidad">

            <ul class="navCenterComunidad">
                <li>
                    <NuxtLink class="textHover" to="/ComunidadPages/Inicio">Inicio</NuxtLink>
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

        <ComunidadPostsIzq></ComunidadPostsIzq>

        <ComunidadPostsDer></ComunidadPostsDer>

        <ComunidadPostsIzq></ComunidadPostsIzq>

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
            .textHover{
                transition: 300ms;
                &:hover {
                    color: #0047ff;
                }

            }
        }
    }
}

.TituloInicioComunidad{
    margin-top: 50px;
    padding: 0px 120px;
    font-size: larger;
}
</style>