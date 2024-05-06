<template>
    <section class="TituloOrden">
        <h1 class="Titulo">Bienvenido a SteamCreate!</h1>
        <div class="OrdenDesc">
            <h3 class="TituloDesc">
                Acerca de:
            </h3>
            <h4 class="DescripcionHome">Steam Workshop es una web centralizada que proporciona contenido creado por los
                usuarios y las herramientas necesarias para publicar, organizar y descargar ese contenido en tus juegos.
                Cada título usará Workshop de distintas formas.</h4>
        </div>
    </section>
</template>

<style lang="postcss">
.TituloOrden {
    display: flex;
    flex-direction: row;
    padding: 100px 150px;
    justify-content: space-between;

    .Titulo {
        font-size: 70px;
        font-weight: 900;
        width: 800px;
    }

    .OrdenDesc {
        .TituloDesc {
            font-size: 25px;
            margin-bottom: 15px
        }

        .DescripcionHome {
            font-size: 10px;
            width: 400px;
        }
    }

}
</style>
<script>
</script>