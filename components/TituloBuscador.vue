<template>
    <section class="TituloOrden">
        <h1 class="Titulo">Comunidad</h1>
        <h4 class="BuscadorTitulo">
            <img class="searchLogo" src="public/Search.svg" alt="">
            <p class="buscarOrden">Busca cualquier cosa...</p>
        </h4>
    </section>
</template>

<style lang="postcss">
.TituloOrden {
    display: flex;
    flex-direction: row;
    padding: 100px 120px;
    justify-content: space-between;

    @media (max-width: 500px) {
        display: flex;
        flex-direction: row;
        padding: 20px 20px;
        justify-content: space-between;
    }

    .Titulo {
        @media (max-width: 500px) {
            font-size: 20px;
        }
    }


    .BuscadorTitulo {
        display: flex;
        flex-direction: row;
        font-size: 8px;
        width: 170px;
        height: 40px;
        align-self: center;
        justify-content: space-between;
        padding: 0px 15px;
        background-color: rgb(33, 33, 33);
        border-radius: 10px;


        .searchLogo {
            height: 20px;
            display: flex;
            align-self: center;
        }

        .buscarOrden {
            display: flex;
            justify-content: center;
            align-self: center;
            color: rgb(159, 159, 159);
            font-size: 10px;
            width: 13i4px;

        }
    }
}
</style>