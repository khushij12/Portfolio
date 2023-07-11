<script setup>
const props = defineProps(["rating"]);
</script>

<template>
    <div class="rating" :style="getRating">
        <div class="rating-fill"></div>
    </div>
</template>
<script>
export default {
    computed: {
        getRating() {
            return {
                '--rating': this.rating,
            }
        }
    }
}
</script>
<style scoped>
.rating {
    width: 400px;
    min-height: 10px;
    background-color: white;
    box-sizing: border-box;
    margin-top: 5px;
}
.rating-fill{
    width: calc(65px * var(--rating));
    background-color: #614c7d;
    min-height: 10px;
}
</style>