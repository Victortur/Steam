<template>
    <section class="OrdenServ">
        <div>
            <img src="public/Servicio1.svg" alt="">
        </div>

        <div class="OrdenServInf">
            <h3>Valve Index</h3>
            <h6 class="white1">Las Valve Index son un avanzado sistema de realidad virtual desarrollado por Valve.
                Ofrecen una
                experiencia inmersiva con pantallas de alta resolución, una tasa de refresco de hasta 144 Hz, y un
                amplio campo de visión. Incluyen controladores ergonómicos que permiten un seguimiento preciso de los
                movimientos de las manos y dedos, proporcionando una interacción natural y detallada en entornos
                virtuales. Diseñadas para ofrecer comodidad y rendimiento superior, las Valve Index son una opción
                destacada para los entusiastas de la realidad virtual que buscan una experiencia de alta calidad.</h6>
            <button class="VerMas1">Ir a la web</button>
        </div>


    </section>
</template>

<style lang="postcss">
.OrdenServ {
    display: flex;
    flex-direction: row;
    transition: 300ms;

    &:hover {
        cursor: pointer;
        transform: scale(102%);
    }

    .OrdenServInf {
        display: flex;
        flex-direction: column;
        width: 70%;
        margin-right: 10%;
        margin-left: 5%;
        justify-content: space-between;
        height: 250px;

        @media (max-width: 500px) {
            display: flex;
            flex-direction: column;
            width: 70%;
            margin-right: 5px;
            margin-left: 5px;
            justify-content: space-between;
            height: 250px;

        }

        .white1 {

            @media (max-width: 500px) {
                font-size: 8px;
            }
        }



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