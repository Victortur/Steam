<template>
    <nav class="ordenNav">
        <ul>
            <li class="Steamlogo">
                <NuxtLink to="/"><img src="public/Steamlogo.svg" alt=""></NuxtLink>
            </li>
        </ul>
        <ul class="navCenter">
            <li>
                <NuxtLink class="textHover" to="/SteamCreate">SteamCreate</NuxtLink>
            </li>
            <li>
                <NuxtLink class="textHover" to="/ComunidadPages/Inicio">Comunidad</NuxtLink>
            </li>
        </ul>
        <ul class="navLeft">
            <li class="InstalarAzul">
                <NuxtLink to="">Instalar</NuxtLink>
            </li>
            <li v-if="!logged && !modalActive">
                <button class="btn-login" @click="toggleModal">
                    Iniciar sesión
                </button>
            </li>
            <li v-else>
                <div class="ordenUser" @click="togglePanel">
                    <div class="user">
                        <img class="iconoUser" src="public/sonic.png" alt="User Icon" />
                    </div>
                    <div class="panel" v-show="panelActive"></div>
                </div>
            </li>
        </ul>

        <!-- Componente Modal -->
        <Modal v-if="modalActive" @close-modal="closeModal" />
    </nav>
</template>

<script setup>
import { ref } from 'vue';
import Modal from './Modal.vue';

const panelActive = ref(false);
const modalActive = ref(false);
const logged = ref(false);

const togglePanel = () => {
    panelActive.value = !panelActive.value;
};

const toggleModal = () => {
    modalActive.value = !modalActive.value;
};

const closeModal = (e) => {
    modalActive.value = false;
    if (e === 'logged') {
        logged.value = true;
    }
};
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

    @media (max-width: 500px) {
        width: 80px;
        align-self: center;
    }
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

    @media (max-width: 500px) {
        padding: 6px 10px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        font-size: 8px;
        border-bottom: solid 0.5px white;
        backdrop-filter: blur(10px);
        position: sticky;
        top: 0;
        z-index: 1000;



    }
}

.navCenter {
    display: flex;
    align-items: center;

    .textHover {
        transition: 300ms;

        &:hover {
            color: #0047ff;
        }
    }
}

.navLeft {
    display: flex;
    align-items: center;

    .InstalarAzul {
        background-color: #0047ff;
        border-radius: 10px;
        margin-right: 10px;
        @media (max-width: 500px) {
            margin-right: 0px;
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
            border-radius: 100%;
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
