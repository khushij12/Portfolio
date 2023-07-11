<script setup>
defineProps({
    text: {
        type: String,
        required: false
    },
    href: {
        type: String,
        required: true
    }
})
</script>

<template>
    <div class="Name">
        <a :href="href"><slot></slot></a>
    </div>
</template>

<style scoped>


.Name:hover {
    color: #e896c0;
    
    transition: 0.3s all;
}
a{
    color: white;
    text-decoration: none;
    border-bottom: 2px solid black;
}
a:hover{
    color: #e896c0;
    border-bottom: 2px solid #e896c0;
    background-color: black;
}
</style>