<template>
    <NuxtLink class="BigArticle" :to="`/gamesdet/${game.id}`">
        <article class="ArticuloPastilla">
            <img class="ImgPastilla" :src="game.background_image" :alt="game.name">
            <div class="ArticuloPastillaInfo">
                <div class="ArticuloName">
                    <h4>{{ game?.name || 'Nombre por defecto' }}</h4>
                    <h6 class="white">¡Atención, fanáticos de Counter-Strike: Global Offensive! Valve ha lanzado una emocionante
                        actualización que trae consigo la esperada Operación Riptide, junto con una serie de mejoras
                        significativas para el modo competitivo.</h6>
                    <h6 class="categ">{{ game?.category || 'Categoría por defecto' }}</h6>
                    <h6 class="fecha">14/03/2024   16:45</h6>
                </div>
            </div>
        </article>
    </NuxtLink>
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
.ArticuloPastilla {
    display: flex;
    flex-direction: row;
    margin: 80px 120px;
    background-color: #111216;
    height: 300px;
    border-radius: 52px;
    transition: 300ms;

    &:hover {
        cursor: pointer;
        transform: scale(102%);
        filter: drop-shadow(0px 0px 30.2px rgba(255, 255, 255, 0.29));
    }

    .ImgPastilla {
        width: 498.34px;
        border-radius: 52px;
        object-fit: cover;
    }

    .ArticuloPastillaInfo {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 500px;
        margin-left: 100px;

        .ArticuloName {
            display: flex;
            align-self: center;
            flex-direction: column;
            .white{
                color: white;
            }
            .categ{
                margin-top: 10px;
            }
            .fecha{
                margin-top: 10px;
            }
        }

        .ArticuloPrice {
            display: flex;
            align-self: center;

        }
    }
}
</style>
