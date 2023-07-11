<script setup>
const props = defineProps(['url', 'logo']);
const image = new URL(`../../assets/${props.logo}`, import.meta.url).href;
</script>
<template>
    <a :href="props.url" target="_blank"><img :src="image" /></a>
</template>
<style scoped>
a {
    background-color: transparent;
    text-decoration: none;
}

a::after {
    background-color: white;
    text-decoration: none;
}
</style>