<template>
    <section class="TituloOrden">
        <h1 class="Titulo">Bienvenido a Steam!</h1>
        <h4 class="DescripcionHome">Tu plataforma definitiva para juegos y entretenimiento! Desde su lanzamiento en
            2003, Steam se ha convertido en el epicentro de la comunidad global de jugadores, ofreciendo una amplia
            variedad de juegos, contenido descargable, y funciones sociales para que disfrutes al máximo de tu
            experiencia de juego</h4>
    </section>
</template>

<style lang="postcss">
.TituloOrden {
    display: flex;
    flex-direction: row;
    padding: 100px 120px;
    justify-content: space-between;

    @media (max-width: 500px) {
        display: flex;
        flex-direction: row;
        padding: 50px 20px;
        justify-content: space-bet
    }

    .DescripcionHome {
        font-size: 8px;
        width: 200px;
        display: flex;
        align-items: center;
    }
}
</style>