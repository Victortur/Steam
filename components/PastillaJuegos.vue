<template>

    <article class="ArticuloPastilla">
        <img class="ImgPastilla" :src="`https://picsum.photos/500/30${count}`" :alt="game.name">
        <div class="ArticuloPastillaInfo">
            <div class="ArticuloName">
                <h4>{{ game?.name || 'Nombre por defecto' }}</h4>
                <h6>{{ game?.category || 'Categoría por defecto' }}</h6>
            </div>
            <div class="ArticuloPrice">
                <h4>$47.99</h4>
            </div>
        </div>
    </article>
    
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
        }

        .ArticuloPrice {
            display: flex;
            align-self: center;

        }
    }
}
</style>
