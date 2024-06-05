<template>
    <section class="IniciarSesion">
        <div id="Sesion" class="Sesion">
            <form @submit.prevent="submitForm" class="InicioGrande">
                <div class="GrandeOrden">
                    <div class="Inicio">
                        <h3 class="colorb">Iniciar Sesión</h3>
                    </div>
                    <div class="Usuario">
                        <div class="Nombre">
                            <h6 class="colorb">Nombre de usuario</h6>
                            <div class="escribir">
                                <input type="text" v-model="formData.name" id="name" placeholder="eg. John98" />
                            </div>
                        </div>
                        <div class="Contraseña">
                            <h6 class="colorb">Contraseña</h6>
                            <div class="escribir">
                                <input type="password" v-model="formData.password" id="password" placeholder="123" />
                            </div>
                        </div>
                    </div>
                    <div class="InicioBoton">
                        <button type="submit">Iniciar Sesión</button>
                    </div>
                </div>
            </form>
            <div class="Registrar">
                <div class="registrarse">
                    <h6 class="colorb">No tienes cuenta?</h6>
                    <h5 class="colorb1">Registrate aquí</h5>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="postcss">
.IniciarSesion {
    display: flex;
    flex-direction: row;
    position: absolute;
    top: 0;
    left: 300px;

    .InicioGrande {
        background-color: white;
        padding: 90px;
        border-radius: 100%;
        width: 500px;
        height: 500px;
        display: flex;
        align-items: center;
        top: 170px;
        left: 27%;
        z-index: 999;
        position: absolute;
        position: fixed;


        .GrandeOrden {
            display: flex;
            justify-content: center;
            flex-direction: column;
            width: 100%;
            height: 250px;
            justify-content: space-between;


            .Inicio {

                .colorb {
                    color: black
                }
            }

            .Usuario {
                .Nombre {
                    margin-bottom: 10px;

                    .colorb {
                        color: black
                    }

                    .escribir {
                        border-radius: 8px;
                        background-color: #04050e;
                        padding: 10px;
                        margin-top: 5px;

                        .colorw {
                            color: white;
                        }
                    }
                }
            }

            .Contraseña {
                .colorb {
                    color: black
                }

                .escribir {
                    border-radius: 8px;
                    background-color: #04050e;
                    padding: 10px;
                    margin-top: 5px;

                    .colorw {
                        color: white;
                    }
                }
            }

            .InicioBoton {
                display: flex;
                justify-content: center;
                width: 150px;
                background-color: #0047ff;
                padding: 10px;
                border-radius: 10px;
            }
        }

    }

    .Registrar {
        background-color: white;
        border-radius: 100%;
        width: 200px;
        padding: 20px;
        height: 200px;
        display: flex;
        align-items: center;
        top: 170px;
        left: 63%;
        z-index: 999;
        position: absolute;
        justify-content: center;
        position: fixed;

        .registrarse {
            display: flex;
            align-items: center;
            flex-direction: column;

            .colorb {
                color: black
            }

            .colorb1 {
                margin-top: 10px;
                font-size: 18px;
                color: black
            }

        }

    }
}
</style>

<script setup>
import { ref } from 'vue';
const emit = defineEmits(["closeModal"]);
const formData = ref({
    name: '',
    password: ''
});

const submitForm = async () => {
    // Verificar las credenciales localmente (simulado)
    if (formData.value.name === 'usuario' && formData.value.password === 'contraseña') {
        // Credenciales válidas, emite el evento de cierre del modal
        emit("closeModal", "logged");
    } else {
        // Credenciales inválidas, mostrar mensaje de error (opcional)
        alert("Nombre de usuario o contraseña incorrectos");
    }
}

const handleCancel = () => {
    emit("closeModal");
};

const closeModal = (e) => {
    emit("closeModal", e);
};
</script>

