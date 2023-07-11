<script setup>
const arr = ["Frontend Developer", "DSA Enthusiast", "Backend Developer", "Creative Art", "Fullstack Developer", "Problem Solving"];
function styleFn(i) {
    return `color:rgb(${Math.random() * 255},${Math.random() * 255}, ${Math.random() * 255
        });animation-delay:${i * 0.1}s;`
}
function AnimalstyleFn(i) {
    return `color:rgb(${Math.random() * 255},${Math.random() * 255}, ${Math.random() * 255
        });animation-delay:${i * 0.05}s;margin:0 20px`
}
</script>


<template>
    <div class="main">
        <div class="intro"><span class="heading">Greetings and welcome to my portfolio! <br>Hi! I'm Khushi Jain.</span><br>
            Frontend and backend developer? Oh, I've got both areas covered like a boss!</div>
        <div><img src="../../assets/F!.png" width="120" height="160" /></div>
    </div>
</template>


<style scoped>
.main {
    height: 95vh;
    background-image: url("../../assets/Untitled.png");
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    gap: 100px;
}

.intro {
    flex-basis: content;
}

.heading {
    font-size: 30px;
    color: #e896c0;
}
</style>