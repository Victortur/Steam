<template>
    <NuxtLink to=""><img src="public/Tienda.svg" alt=""></NuxtLink>
</template>

<style lang="postcss">
.header-image{
    width: 100%;
    height: 250px;
    object-fit: cover;
}
</style>

<script setup>
    const props = defineProps({
        source: {
            type: String,
            required: false
        },
    });
    const { source } = props;
</script>