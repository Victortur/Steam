<template>
    <section class="SectionComunidad">

        <div class="SectionArticles">
            <div class="ArticlesLeft">
                <article class="BigArticle">
                    <h4>Elite Dangerous</h4>
                    <div class="UserInfo">
                        <div class="ProfileiconOrden">
                            <img class="Profileicon" src="public/Profileicon.svg" alt="">
                            <h5>Mateo</h5>
                        </div>
                        <h6>Posted on 12 Sept 2023</h6>
                    </div>
                    <img src="public/imgJuego3.png" alt="">
                    <div class="UserInfo1">
                        <h6>A game made for artists</h6>
                        <div>
                            <img src="public/likeImg.svg" alt="">
                        </div>
                    </div>
                </article>


                <article class="SmallArticle">
                    <h4>Elite Dangerous</h4>
                    <div class="UserInfo">
                        <div class="ProfileiconOrden">
                            <img class="Profileicon" src="public/Profileicon.svg" alt="">
                            <h5>Mateo</h5>
                        </div>
                        <h6>Posted on 12 Sept 2023</h6>
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


<style lang="postcss">
.SectionComunidad {
    display: flex;
    flex-direction: column;
    padding: 30px 120px;

    .SectionTitle {}

    .SectionArticles {

        .ArticlesLeft {
            padding: 30px 0px;
            display: flex;
            flex-direction: row;

            .BigArticle {
                background-color: #111216;
                padding: 20px;
                width: 60%;
                border-radius: 32px;
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
                .ImgArticleSmall{
                    height: 426.44px;
                    border-radius: 28px;
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