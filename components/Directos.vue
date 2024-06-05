<template>
    <div class="OrdenDirecto11">
        <div class="OrdenDirecto1">
            <div class="OrdenDirecto21">
                <img src="public/illojuan.svg" alt="directoIlloJuan">

                <div class="DirectoInfo1">
                    <div>
                        <img class="ImgStream1" src="public/illo2Circulo.svg" alt="">
                    </div>
                    <div class="NombreStream1">
                        <h5 class="tituloMovil">Jugando a Red Dead Redemption!!</h5>
                        <h6 class="tituloMovil">Illojuan</h6>

                    </div>
                </div>
            </div>
            <div class="OrdenDirecto21">
                <img src="public/illojuan.svg" alt="directoIlloJuan">

                <div class="DirectoInfo1">
                    <div>
                        <img class="ImgStream1" src="public/illo2Circulo.svg" alt="">
                    </div>
                    <div class="NombreStream1">
                        <h5 class="tituloMovil">Jugando a Red Dead Redemption!!</h5>
                        <h6 class="tituloMovil">Illojuan</h6>

                    </div>
                </div>
            </div>
        </div>
    </div>

</template>

<style lang="postcss">
.OrdenDirecto11 {
    width: 100%;
    display: flex;
    justify-content: center;

    .OrdenDirecto1 {
        display: flex;
        flex-direction: row;
        justify-content: center;
        margin-top: 40px;
        width: 1000px;
        justify-content: space-between;

        @media (max-width: 500px) {
            display: flex;
            flex-direction: row;
            justify-content: center;
            margin-top: 20px;
            width: 90%;
            justify-content: space-between;


        }

        .OrdenDirecto21 {
            width: 490px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            padding: 20px;
            border-radius: 40px;
            background-color: rgba(17, 18, 22, 1);
            transition: 300ms;

            &:hover {
                cursor: pointer;
                transform: scale(102%);
                filter: drop-shadow(0px 0px 30.2px rgba(255, 255, 255, 0.29));
            }

            .DirectoInfo1 {
                display: flex;
                flex-direction: row;
                margin-top: 20px;

                .ImgStream1 {
                    width: 40px;
                    display: flex;
                    align-self: center;
                }

                .NombreStream1 {
                    margin-left: 20px;

                    .tituloMovil {
                        @media (max-width: 500px) {
                            font-size: 14px;
                        }

                    }
                }
            }
        }


    }
}
</style>