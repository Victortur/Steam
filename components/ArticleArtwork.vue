<template>
    <article class="ArticleArtwork">
        <img class="imgArtwork" src="public/imgJuego6Art.png" alt="">
        <div class="OrdenArtwork">
            <div>
                <div class="UserInfo1">
                    <div class="ProfileiconOrden1">
                        <img class="Profileicon1" src="public/Profileicon.svg" alt="">
                        <h5>Mateo</h5>
                    </div>
                    <h6>Posted on 12 Sept 2023</h6>
                </div>
                <div class="OrdenInfoArtwork">
                    <h4 class="MasPeq">Creado en: It takes two</h4>
                    <h6>Los Sueños. El LSPD informa de un gran aumento de los delitos en toda el área metropolitana de
                        Los
                        Sueños. Los SWAT tratan de solventar situaciones de alto riesgo como tomas de rehenes, amenazas
                        de
                        bomba y sospechosos atrincherados, entre otros.</h6>
                </div>
            </div>
            <div class="IconosArtOrden">
                <img class="IconosArt" src="public/IconosArt.svg" alt="">
            </div>
        </div>

    </article>

    <article class="ArticleArtwork1">
        <img class="imgArtwork" src="public/imgJuego6Art2.png" alt="">
        <div class="OrdenArtwork">
            <div>
                <div class="UserInfo1">
                    <div class="ProfileiconOrden1">
                        <img class="Profileicon1" src="public/Profileicon.svg" alt="">
                        <h5>Mateo</h5>
                    </div>
                    <h6>Posted on 12 Sept 2023</h6>
                </div>
                <div class="OrdenInfoArtwork">
                    <h4 class="MasPeq">Creado en: It takes two</h4>
                    <h6>Los Sueños. El LSPD informa de un gran aumento de los delitos en toda el área metropolitana de
                        Los
                        Sueños. Los SWAT tratan de solventar situaciones de alto riesgo como tomas de rehenes, amenazas
                        de
                        bomba y sospechosos atrincherados, entre otros.</h6>
                </div>
            </div>
            <div class="IconosArtOrden">
                <img class="IconosArt" src="public/IconosArt.svg" alt="">
            </div>
        </div>

    </article>


    <article class="ArticleArtwork2">
        <img class="imgArtwork" src="public/imgJuego5.png" alt="">
        <div class="OrdenArtwork">
            <div>
                <div class="UserInfo1">
                    <div class="ProfileiconOrden1">
                        <img class="Profileicon1" src="public/Profileicon.svg" alt="">
                        <h5>Mateo</h5>
                    </div>
                    <h6>Posted on 12 Sept 2023</h6>
                </div>
                <div class="OrdenInfoArtwork">
                    <h4 class="MasPeq">Creado en: It takes two</h4>
                    <h6>Los Sueños. El LSPD informa de un gran aumento de los delitos en toda el área metropolitana de
                        Los
                        Sueños. Los SWAT tratan de solventar situaciones de alto riesgo como tomas de rehenes, amenazas
                        de
                        bomba y sospechosos atrincherados, entre otros.</h6>
                </div>
            </div>
            <div class="IconosArtOrden">
                <img class="IconosArt" src="public/IconosArt.svg" alt="">
            </div>
        </div>

    </article>
</template>

<style lang="postcss">
.ArticleArtwork {
    display: flex;
    flex-direction: row;
    padding: 80px 120px;
    transition: 300ms;

    @media (max-width: 500px) {
        padding: 30px 10px;
    }

    &:hover {
        cursor: pointer;
        transform: scale(102%);
    }

    .imgArtwork {
        width: 900px;
        margin-right: 15px;

        @media (max-width: 500px) {
            width: 50%;
            height: 370px;
            margin-right: 5px;
            object-fit: cover;
            border-radius: 6px;
        }
    }

    .OrdenArtwork {
        display: flex;
        flex-direction: column;
        width: 400px;
        justify-content: space-between;

        .UserInfo1 {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            margin-bottom: 20px;
            align-items: center;

            @media (max-width: 500px) {
                display: flex;
                flex-direction: column;
                margin-bottom: 20px;
                align-items: center;
            }

            .ProfileiconOrden1 {
                display: flex;
                flex-direction: row;

                .Profileicon1 {
                    margin-right: 10px;
                    width: 15px;

                    @media (max-width: 500px) {
                        margin-right: 10px;
                        width: 10px;
                    }
                }
            }
        }

        .OrdenInfoArtwork {
            .MasPeq {
                @media (max-width: 500px) {
                    font-size: 12px;
                }
            }
        }

        .IconosArtOrden {
            display: flex;

            .IconosArt {
                width: 200px;
            }

        }
    }

}

.ArticleArtwork1 {
    display: flex;
    flex-direction: row;
    padding: 0px 120px 80px 120px;
    transition: 300ms;
    @media (max-width: 500px) {
        padding: 30px 10px;
    }

    &:hover {
        cursor: pointer;
        transform: scale(102%);
    }

    .imgArtwork {
        margin-right: 15px;
        height: 347.94px;
        @media (max-width: 500px) {
            width: 50%;
            height: 370px;
            margin-right: 5px;
            object-fit: cover;
            border-radius: 6px;
        }
    }

    .OrdenArtwork {
        display: flex;
        flex-direction: column;
        width: 400px;
        justify-content: space-between;

        .UserInfo1 {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            margin-bottom: 20px;
            align-items: center;
            @media (max-width: 500px) {
                display: flex;
                flex-direction: column;
                margin-bottom: 20px;
                align-items: center;
            }

            .ProfileiconOrden1 {
                display: flex;
                flex-direction: row;

                .Profileicon1 {
                    margin-right: 10px;
                    width: 15px;
                    @media (max-width: 500px) {
                        margin-right: 10px;
                        width: 10px;
                    }
                }
            }
        }

        .OrdenInfoArtwork {
            .MasPeq {
                @media (max-width: 500px) {
                    font-size: 12px;
                }
            }
        }
    }

}

.ArticleArtwork2 {
    display: flex;
    flex-direction: row;
    padding: 0px 120px 80px 120px;
    transition: 300ms;
    @media (max-width: 500px) {
        padding: 30px 10px;
    }

    &:hover {
        cursor: pointer;
        transform: scale(102%);
    }

    .imgArtwork {
        width: 900px;
        margin-right: 15px;
        @media (max-width: 500px) {
            width: 50%;
            height: 370px;
            margin-right: 5px;
            object-fit: cover;
            border-radius: 6px;
        }
    }

    .OrdenArtwork {
        display: flex;
        flex-direction: column;
        width: 400px;
        justify-content: space-between;

        .UserInfo1 {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            margin-bottom: 20px;
            align-items: center;
            @media (max-width: 500px) {
                display: flex;
                flex-direction: column;
                margin-bottom: 20px;
                align-items: center;
            }

            .ProfileiconOrden1 {
                display: flex;
                flex-direction: row;

                .Profileicon1 {
                    margin-right: 10px;
                    width: 15px;
                    @media (max-width: 500px) {
                        margin-right: 10px;
                        width: 10px;
                    }
                }
            }
        }

        .OrdenInfoArtwork {
            .MasPeq {
                @media (max-width: 500px) {
                    font-size: 12px;
                }
            }
        }
    }

}
</style>