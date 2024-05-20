<template>
    <section class="SectionComunidad1">

        <div class="SectionArticles1">
            <div class="ArticlesLeft1">

                <article class="SmallArticle1">
                    <h4>Elite Dangerous</h4>
                    <div class="UserInfo1">
                        <div class="ProfileiconOrden1">
                            <img class="Profileicon1" src="public/Profileicon.svg" alt="">
                            <h5>Mateo</h5>
                        </div>
                        <h6>Posted on 12 Sept 2023</h6>
                    </div>
                    <img class="ImgArticleSmall1" src="public/imgJuego1.svg" alt="">
                    <div class="UserInfo11">
                        <h6>A game made for artists</h6>
                        <div>
                            <img src="public/likeImg.svg" alt="">
                        </div>
                    </div>
                </article>

                <article class="BigArticle1">
                    <h4>Elite Dangerous</h4>
                    <div class="UserInfo1">
                        <div class="ProfileiconOrden1">
                            <img class="Profileicon1" src="public/Profileicon.svg" alt="">
                            <h5>Mateo</h5>
                        </div>
                        <h6>Posted on 12 Sept 2023</h6>
                    </div>
                    <img src="public/imgArticle1.svg" alt="">
                    <div class="UserInfo11">
                        <h6>A game made for artists</h6>
                        <div>
                            <img src="public/likeImg.svg" alt="">
                        </div>
                    </div>
                </article>

            </div>

        </div>

    </section>
</template>


<style lang="postcss">
.SectionComunidad1 {
    display: flex;
    flex-direction: column;
    padding: 0px 120px;

    .SectionTitle1 {}

    .SectionArticles1 {

        .ArticlesLeft1 {
            display: flex;
            flex-direction: row;

            .BigArticle1 {
                background-color: #111216;
                padding: 20px;
                width: 60%;
                border-radius: 32px;
                .UserInfo1 {
                    margin-top: 20px;
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    margin-bottom: 20px;
                    align-items: center;


                    .ProfileiconOrden1 {
                        display: flex;
                        flex-direction: row;
                        .Profileicon1 {
                            margin-right: 10px;
                            width: 15px;
                        }
                    }
                }
                .UserInfo11 {
                    margin-top: 20px;
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;   
                    align-items: center;                     
                }

            }

            .SmallArticle1 {
                background-color: #111216;
                padding: 20px;
                margin-right: 15px;
                width: 40%;
                border-radius: 32px;
                .ImgArticleSmall1{
                    height: 426.44px;
                    border-radius: 28px;
                }
                .UserInfo1 {
                    margin-top: 20px;
                    display: flex;
                    flex-direction: row;
                    justify-content: space-between;
                    margin-bottom: 20px;
                    align-items: center;     
                    .ProfileiconOrden1 {
                        display: flex;
                        flex-direction: row;
                        .Profileicon1 {
                            margin-right: 10px;
                            width: 15px;
                        }
                    }

                }
                .UserInfo11 {
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