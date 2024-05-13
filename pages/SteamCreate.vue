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

    <section class="crearOrden">
        <div class="crear">
            <p>Crear</p>
        </div>
        <div class="explorar">
            <p>Explorar</p>
        </div>
    </section>

    <section class="ordenDescAbajo">
        <div class="ordenIzq">
            <h4 class="DescripcionHome1">El Workshop de Steam es una web centralizada que proporciona contenido creado
                por los usuarios y las herramientas necesarias para publicar, organizar y descargar ese contenido en tus
                juegos. Cada título utiliza el Workshop de distintas formas.

                Algunos juegos, como «Team Fortress 2», permiten crear y presentar nuevos artículos (como sombreros,
                armas, insignias, botas y mucho más) para que se considere la posibilidad de incorporarlos al juego.
                Otros, como «The Elder Scrolls V: Skyrim», permiten a los creadores de mods publicar sus trabajos
                directamente en el Workshop para que los jugadores puedan suscribirse a los que quieran usar en el
                juego.
            </h4>
        </div>
        <div class="ordenDer">
            <h4 class="DescripcionHome1">El Workshop de Steam es una web centralizada que proporciona contenido creado
                por los usuarios y las herramientas necesarias para publicar, organizar y descargar ese contenido en tus
                juegos. Cada título utiliza el Workshop de distintas formas.

                Algunos juegos, como «Team Fortress 2», permiten crear y presentar nuevos artículos (como sombreros,
                armas, insignias, botas y mucho más) para que se considere la posibilidad de incorporarlos al juego.
                Otros, como «The Elder Scrolls V: Skyrim», permiten a los creadores de mods publicar sus trabajos
                directamente en el Workshop para que los jugadores puedan suscribirse a los que quieran usar en el
                juego.El Workshop de Steam es una web centralizada que proporciona contenido creado
                por los usuarios y las herramientas necesarias para publicar, organizar y descargar ese contenido en tus
                juegos. Cada título utiliza el Workshop de distintas formas.

                Algunos juegos, como «Team Fortress 2», permiten crear y presentar nuevos artículos (como sombreros,
                armas, insignias, botas y mucho más) para que se considere la posibilidad de incorporarlos al juego.
                Otros, como «The Elder Scrolls V: Skyrim», permiten a los creadores de mods publicar sus trabajos
                directamente en el Workshop para que los jugadores puedan suscribirse a los que quieran usar en el
                juego.
            </h4>
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
        display: flex;
        flex-direction: column;

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

.crearOrden {
    display: flex;
    flex-direction: row;
    margin: 0px 150px;
    justify-content: space-between;

    .crear {
        display: flex;
        justify-content: center;
        align-items: end;
        padding-bottom: 10px;
        width: 600px;
        height: 200px;
        background-color: #181a1f;
        border-radius: 20px;
    }

    .explorar {
        display: flex;
        justify-content: center;
        align-items: end;
        padding-bottom: 10px;
        width: 600px;
        height: 200px;
        background-color: #181a1f;
        border-radius: 20px;
    }
}

.ordenDescAbajo{
    display: flex;
    flex-direction: row;
    padding: 100px 150px;

    .ordenIzq{
        margin: 10px;
        width: 400px;
        .DescripcionHome1{
            font-size: 10px;
        }
    }
    .ordenDer{
        margin: 10px;
        width: 400px;
        .DescripcionHome1{
            font-size: 10px;
        }
    }
}
</style>
<script>
</script>