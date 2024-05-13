<template>
    <nav class="ordenNav">
        <ul>
            <li class="Steamlogo">
                <NuxtLink to="/about"><img src="public/Steamlogo.svg" alt=""></NuxtLink>
            </li>
        </ul>
        <ul class="navCenter">
            <li>
                <NuxtLink to="/SteamCreate">SteamCreate</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/">Tienda</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/ComunidadPages/Inicio">Comunidad</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/">Users</NuxtLink>
            </li>
        </ul>
        <ul class="navLeft">
            <li>
                <NuxtLink to="/about">Instalar</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/about">Mateo</NuxtLink>
            </li>
            <li>
                <div class="ordenUser">
                    <div class="user" @click="panelActive = !panelActive">
                        <Icon class="iconoUser" name="ic:baseline-account-circle" />
                    </div>

                    <div class="panel" v-show="panelActive">
                    </div>
                </div>
            </li>
        </ul>

    </nav>
</template>

<script setup>
import { ref } from 'vue'
const panelActive = ref(false)
</script>

<style lang="postcss">
ul {
    @apply flex p-4;

    li {
        @apply p-4;
    }
}

.Steamlogo {
    width: 150px;


}

.ordenNav {
    padding: 10px 60px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-size: 13px;
    border-bottom: solid 0.5px white;

    .navCenter {
        display: flex;
        align-items: center;
    }

    .navLeft {
        display: flex;
        align-items: center;
    }


}

.ordenUser {
    display: flex;
    flex-direction: column;
    height: 40px;
    width: 40px;

    .user {
        height: 40px;
        width: 40px;

        .iconoUser {
            height: 40px;
            width: 40px;
        }
    }
}

.panel {
    position: absolute;
    display: flex;
    flex-direction: column;
    background-color: aqua;
    width: 300px;
    top: 90px;
    right: 0px;
    height: 300px;
}
</style>
