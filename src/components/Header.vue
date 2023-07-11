<script setup>
import Links from './ThemeElement/Links.vue';
import Character from "../assets/Character.vue";
</script>

<template>
    <div style="position: sticky; top: 0;z-index: 1000;">
        <div class="head">
            <div class="name">
                <!-- <Character /> -->
                <!-- <Char /> -->

                <h4>
                    <Links href="#"><span class="bracket">{</span> <span class="abbr">KJ</span> <span class="bracket">}</span></Links>
                </h4>
            </div>
            <div class="nav">
                <button type="button" class="btn btn-dark" @click="scroll('exp')">
                    <i class="bi bi-book"></i> Experience
                </button>
                <button type="button" class="btn btn-dark" @click="scroll('qual')"><i class="bi bi-journal" ></i>
                    Education</button>
                <button type="button" class="btn btn-dark" @click="scroll('skill')"><i class="bi bi-trophy" ></i>
                    Skills</button>
                <button type="button" class="btn btn-dark" @click="scroll('proj')"><i class="bi bi-pc-display" ></i>
                    Projects</button>
                <button type="button" class="btn btn-dark" @click="scroll('contact')"><i class="bi bi-telephone" ></i>
                    Contact</button>
            </div>
        </div>
    </div>
</template>

<script>

function scroll(className) {
    document.querySelector("." + className).scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'start' });
}
</script>
<style scoped>
.head {
    display: flex;
    justify-content: space-between;
    padding: 0 15px;
    height: 8vh;
    color: white;
    background-color: black;
    align-items: center;
    box-shadow: 0 -2px 10px #786976;
}

.nav {
    display: flex;
    gap: 10px;
    align-items: center;
}

button {
    background-color: black;
}

button:hover {
    color: #e896c0;
}
.bracket{
    font-weight: 900;
    color: rgb(197, 197, 197);
}
.abbr{
    color: #e896c0;
    font-weight: 500;
}
</style>

