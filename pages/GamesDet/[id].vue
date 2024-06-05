<template>
    <div v-if="data != null">
        <ImageDet :source="data.background_image" />
        <main class="container">
            <h1>{{data.name}}</h1>
            <p v-html="data.description">
                
            </p>
        </main>
    </div>
</template>

<script setup >

    const route = useRoute();
    const { data } = useFetch(`https://api.rawg.io/api/games/${route.params.id}?key=ed55e0ad388f4039b1f1f7b96d735708`)

</script>