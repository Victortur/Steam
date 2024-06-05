<template>
    <section class="SectionComunidad">

        <div class="SectionArticles">
            <div class="ArticlesLeft">
                <NuxtLink class="BigArticle" :to="`/gamesdet/${game.id}`">
                    <article>
                        <h4>{{ game?.name || 'Nombre por defecto' }}</h4>
                        <div class="UserInfo">
                            <div class="ProfileiconOrden">
                                <img class="Profileicon" src="public/Profileicon.svg" alt="">
                                <h5>Mateo</h5>
                            </div>
                            <h6>{{ game?.updated || 'Fecha por defecto' }}</h6>
                        </div>
                        <img src="public/imgJuego3.png" alt="">
                        <div class="UserInfo1">
                            <h6>A game made for artists</h6>
                            <div>
                                <img src="public/likeImg.svg" alt="">
                            </div>
                        </div>
                    </article>
                </NuxtLink>

                <article class="SmallArticle">
                    <h4>{{ game?.name || 'Nombre por defecto' }}</h4>
                    <div class="UserInfo">
                        <div class="ProfileiconOrden">
                            <img class="Profileicon" src="public/Profileicon.svg" alt="">
                            <h5>Mateo</h5>
                        </div>
                        <h6>{{ game?.updated || 'Fecha por defecto' }}</h6>
                    </div>
                    <img class="ImgArticleSmall" src="public/imgJuego1.svg" alt="">
                    <div class="UserInfo1">
                        <h6>A game made for artists</h6>
                        <div>
                            <img src="public/likeImg.svg" alt="">
                        </div>
                    </div>
                </article>

            </div>


            <div class="ArticlesRight"></div>
        </div>

    </section>
</template>


<script setup>
const props = defineProps({
    game: {
        type: Object,
        default: () => ({ name: 'Nombre por defecto', category: 'Categoría por defecto', price: 'Precio por defecto' })
    },
    count: {
        type: Number,
    }
});
const { game } = props;
const { count } = props;
</script>

<style lang="postcss">
.SectionComunidad {
    display: flex;
    flex-direction: column;
    padding: 30px 120px;

    @media (max-width: 500px) {
        display: flex;
        flex-direction: column;
        padding: 10px 10px;
    }

    .SectionTitle {}

    .SectionArticles {

        .ArticlesLeft {
            padding: 30px 0px;
            display: flex;
            flex-direction: row;

            @media (max-width: 500px) {
                display: flex;
                flex-direction: column;
                padding: 10px 0px;
            }

            .BigArticle {
                background-color: #111216;
                padding: 20px;
                width: 60%;
                border-radius: 32px;
                transition: 300ms;

                @media (max-width: 500px) {
                    width: 100%;
                    margin-bottom: 60px;
                    padding: 5px;
                    width: 100%;
                    border-radius: 32px;
                    transition: 300ms;
                }

                &:hover {
                    cursor: pointer;
                    transform: scale(102%);

                    img {
                        filter: drop-shadow(0px 0px 103.2px rgba(255, 255, 255, 0.29));
                    }
                }

                .UserInfo {
                    margin-top: 20px;
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    margin-bottom: 20px;
                    align-items: center;


                    .ProfileiconOrden {
                        display: flex;
                        flex-direction: row;

                        .Profileicon {
                            width: 15px;
                            margin-right: 10px;
                        }
                    }
                }

                .UserInfo1 {
                    margin-top: 20px;
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    align-items: center;
                }

            }

            .SmallArticle {
                background-color: #111216;
                padding: 20px;
                margin-left: 15px;
                width: 40%;
                border-radius: 32px;
                transition: 300ms;


                @media (max-width: 1000px) {
                    width: 100%;
                    margin-left: 0px;
                    background-color: #111216;
                    padding: 5px;
                    width: 100%;

                }

                &:hover {
                    cursor: pointer;
                    transform: scale(102%);

                    img {
                        filter: drop-shadow(0px 0px 103.2px rgba(255, 255, 255, 0.29));
                    }
                }

                .ImgArticleSmall {
                    height: 426.44px;
                    border-radius: 28px;

                    @media (max-width: 1000px) {
                        max-height: 703px;
                        width: 100%;
                        object-fit: cover;
                        height: 212px;
                    }
                }

                .UserInfo {
                    margin-top: 20px;
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    margin-bottom: 20px;
                    align-items: center;

                    .ProfileiconOrden {
                        display: flex;
                        flex-direction: row;

                        .Profileicon {
                            margin-right: 10px;
                            width: 15px;
                        }
                    }

                }

                .UserInfo1 {
                    margin-top: 20px;
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    align-items: center;
                }
            }

        }

    }




}
</style>
