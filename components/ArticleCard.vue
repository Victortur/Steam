<template>
    <article>
    <img :src="article.url" :alt="article.title">
    <button>{{article.title}}</button>
    <Icon name="svg-spinners:12-dots-scale-rotate" color="black" />
</article>
</template>

<style lang="postcss">
    article{
        width: 300px;
        img{
            width: 100%;
            object-fit: cover;
        }
        button{
            @apply p-5 bg-gray-200 w-full;
            text-align: center;
        }
    }
</style>

<script setup>
const props= defineProps({
    article:{
        type: Object,
        required: false
    }
});
const{article} = props;

</script>