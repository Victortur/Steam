<template>
  <div class="body">
    <NavBar />
    <NuxtPage />
  </div>
</template>



<style lang="postcss">
@tailwind base;


*{
  color: #fff;
  font-family: Poppins;
}

.body{
  @apply bg-[--color-bg];
}

@layer base {
  :root {
    --color-bg: #04050e;
    --color-primary: #0047ff;
  }
}
</style>

