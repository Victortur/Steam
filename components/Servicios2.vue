<template>
    <section class="OrdenServ1">
        <div class="OrdenServInf1">
            <h3>Steam deck</h3>
            <h6 class="white">El Steam Deck es una consola portátil desarrollada por Valve que permite jugar a juegos de
                PC en cualquier lugar. Equipada con un hardware potente, incluye una pantalla táctil de 7 pulgadas, un
                procesador AMD personalizado, y controles integrados como joysticks, botones y trackpads. El dispositivo
                ejecuta SteamOS, una versión de Linux optimizada para juegos, y ofrece acceso completo a la biblioteca
                de Steam. Con su diseño ergonómico y capacidad para conectar periféricos y monitores externos, el Steam
                Deck combina la versatilidad de una PC con la comodidad de una consola portátil, ofreciendo una
                experiencia de juego flexible y de alta calidad.</h6>
            <button class="VerMas1">Ir a la web</button>
        </div>

        <div>
            <img src="public/Servicio2.svg" alt="">
        </div>

    </section>
</template>

<style lang="postcss">
.OrdenServ1 {
    display: flex;
    flex-direction: row;
    margin-top: 40px;
    margin-bottom: 40px;
    transition: 300ms;
    &:hover {
        cursor: pointer;
        transform: scale(102%);
    }

    .OrdenServInf1 {
        display: flex;
        flex-direction: column;
        width: 70%;
        margin-right: 5%;
        margin-left: 10%;
        justify-content: space-between;
        height: 250px;

        .VerMas1 {
            font-size: 13px;
            background-color: #0047ff;
            padding: 10px;
            border-radius: 10px;
            width: 200px;
        }
    }

}
</style>