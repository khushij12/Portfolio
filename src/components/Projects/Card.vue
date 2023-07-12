<script setup>
const props = defineProps(['name', 'techStack', 'desc', 'link', 'image-link', 'color']);
const image = new URL(`../../assets/${props['imageLink']}`, import.meta.url).href;
</script>

<template>
    <a :href="props.link">
        <div class="card">
            <p class="card-title">{{ props.name }}</p>
            <div class="card-image"><img :src="image" /></div>
            <div class="card-link"></div>
            <div class="card-tags">
                <div v-for="ts in props.techStack" class="card-tags-box"
                    :style="{ color: `rgb(${props.color[0]},${props.color[1]},${props.color[2]})`, backgroundColor: `rgba(${props.color[0]},${props.color[1]},${props.color[2]},0.2)` }">
                    {{ ts }}
                </div>
            </div>
            <p class="card-desc">{{ props.desc }}</p>
            <!-- <p>{{ props.link }}</p> -->
        </div>
    </a>
</template>

<style scoped>
.card-tags {
    display: flex;
    flex-direction: row;
    gap: 10px;
}

.card-tags-box {
    width: max-content;
    border-radius: 5px;
    padding: 3px 10px;
    font-size: 15px;
}

.card {
    width: 409px;
    min-height: 385px;
    border-radius: 25px;
    background: black;
    color: white;
    padding: 20px 13px 10px 13px;
    display: flex;
    gap: 10px;
}

.card:hover {
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

.card-image {
    height: 160px;
    border-radius: 15px;
    width: 380px;
    margin: auto;
}

img {
    width: 100%;
    height: 100%;
    border-radius: 15px;
    object-fit: cover;
    object-position: 50% 50%;
}

.card-desc {
    font-size: 15px;
    color: rgb(197, 197, 197);
}

/* .card-link{
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background-color: white;
    align-self: flex-end;
} */
a {
    text-decoration: none;
}

a::after {
    text-decoration: none;
}
</style>