<template>
    <nav class="ordenNav">
        <ul>
            <li class="Steamlogo">
                <NuxtLink to="/Home"><img src="public/Steamlogo.svg" alt=""></NuxtLink>
            </li>
        </ul>
        <ul class="navCenter">
            <li>
                <NuxtLink class="textHover" to="/SteamCreate">SteamCreate</NuxtLink>
            </li>
            <li>
                <NuxtLink class="textHover" to="/">Tienda</NuxtLink>
            </li>
            <li>
                <NuxtLink class="textHover" to="/ComunidadPages/Inicio">Comunidad</NuxtLink>
            </li>
            <li>
                <NuxtLink class="textHover" to="/">Users</NuxtLink>
            </li>
        </ul>
        <ul class="navLeft">
            <li class="InstalarAzul">
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
    align-self: center;
}

.ordenNav {
    padding: 10px 60px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-size: 13px;
    border-bottom: solid 0.5px white;
    backdrop-filter: blur(10px);
    position: sticky;
    top: 0;
    z-index: 1000;

    .navCenter {
        display: flex;
        align-items: center;
        .textHover{
            transition: 300ms;
                &:hover {
                    color: #0047ff;
                }
        }
    }

    .navLeft {
        display: flex;
        align-items: center;
        .InstalarAzul{
            background-color: #0047ff;
            border-radius: 10px;
        }
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
