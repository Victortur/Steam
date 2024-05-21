<template>

    <article class="ArticuloPastilla">
        <img src="public/PastillaJuego.svg" alt="">
        <div class="ArticuloPastillaInfo">
            <div class="ArticuloName">
                <h4>Black Ops 4</h4>
                <h6>Call of Duty</h6>
            </div>
            <div class="ArticuloPrice">
                <h4>$47.99</h4>
            </div>
        </div>
    </article>

</template>


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
