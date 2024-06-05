<script setup lang="ts">
</script>

<template>
  <div class="body">
    <NavBar />
    <NuxtPage />
    <IniciarSesion></IniciarSesion>
    <Footer v-if="$route.path !== '/IniciarSesion'"></Footer>
  </div>
</template>



<style lang="postcss">
@tailwind base;


* {
  color: #fff;
  font-family: Poppins;
//border: 1px solid red;

}

h1 {
  font-size: 86px;
  font-weight: 900;
}

h2{
  font-size: 54px;
}

h3{
  font-size: 32px;
}

h4{
  font-size: 26px;
}

h5{
  font-size: 20px;
}

h6 {
  font-size: 12px;
  color: #76808C;
}


.body {
  @apply bg-[--color-bg];
}

@layer base {
  :root {
    --color-bg: #04050e;
    --color-primary: #0047ff;
  }
}

</style>
