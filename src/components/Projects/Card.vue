<script setup>
const props = defineProps(['name', 'desc', 'link', 'image-link']);
const image = "url(/src/assets/" + props['imageLink']+")";
</script>

<template>
    <a :href="props.link">
    <div class="card">
        <p class="card-title">{{ props.name }}</p>
        <div class="card-image"></div>
        <div class="card-link"></div>
        <p class="card-desc">{{ props.desc }}</p>
        <!-- <p>{{ props.link }}</p> -->
    </div>
</a>
</template>

<style scoped>
.card {
    width: 409px;
    height: 385px;
    border-radius: 25px;
    background: black;
    
    color: white;
    padding: 20px 13px 10px 13px;
    display: flex;
    gap: 10px;
}

.card:hover{
    /* animation: bigCircle 3s; */
    /* box-shadow: 0px 4px 4px 0px rgba(255, 255, 255, 0.25); */
    filter: drop-shadow(1px 3px 14px rgba(255, 255, 255, 0.25));
    transition: 0.3s all;
}

img {
    background-size: cover;
}

.card-title {
    color: white;
    font-weight: 700;
    font-size: 22px;
    letter-spacing: -0.055px;
}

.card-image{
    background-image: v-bind("image");
    background-size: cover;
    background-position: 12%;
    height: 160px;
    border-radius: 15px;
    width: 380px;
    margin: auto;
    z-index: 23;
    position: relative;
}
.card-desc{
    font-size: 15px;
    color: rgb(197,197,197);
}
/* .card-link{
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background-color: white;
    align-self: flex-end;
} */
a{
    text-decoration: none;
}
a::after{
    text-decoration: none;
}
</style>