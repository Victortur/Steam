<template>
    <article class="ArticleArtwork3">
        <img class="imgArtwork" src="public/imgJuego7.png" alt="">
        <div class="OrdenArtLargo">
            <div class="OrdenArtwork">
                <div class="UserInfo1">
                    <div class="ProfileiconOrden1">
                        <img class="Profileicon1" src="public/Profileicon.svg" alt="">
                        <h5>Mateo</h5>
                    </div>
                    <h6>Posted on 12 Sept 2023</h6>
                </div>
                <div class="OrdenInfoArtwork">
                    <h4>Creado en: It takes two</h4>
                </div>
            </div>
            <div class="IconosArtOrden">
                <img class="IconosArt" src="public/IconosArt.svg" alt="">
            </div>
        </div>

    </article>
</template>

<style lang="postcss">

.ArticleArtwork3 {
    display: flex;
    flex-direction: column;
    padding: 80px 120px;

    .imgArtwork {}

    .OrdenArtLargo {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        margin-top: 15px;
        .OrdenArtwork {
            display: flex;
            flex-direction: row;

            .UserInfo1 {
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                width: 300px;
                margin-right: 15px;

                .ProfileiconOrden1 {
                    display: flex;
                    flex-direction: row;

                    .Profileicon1 {
                        margin-right: 10px;
                        width: 15px;
                    }
                }
            }

            .OrdenInfoArtwork {}

            .IconosArtOrden {
                display: flex;
                align-self: flex-end;

                .IconosArt {
                    width: 200px;
                }

            }
        }
    }

}

</style>