<script setup>
import Skill from "../../constants/skills";
import Rating from "./Rating.vue";
</script>
<template>
    <div class="skill">
        <div class="skill-head">
            SKILLS
        </div>
        <div class="skill-content">
            <div class="skill-content-box">

                <span>{{ 'Backend Development' }}</span>
                <div v-for="skill of Object.entries(Skill['Backend Development'])" class="skill-content-box-content">
                    {{ skill[1].name }}
                    <Rating :rating="skill[1].rating" />
                </div>

            </div>

            <!-- <div class="skill-content-box">
                <span>{{ 'Mobile Development' }}</span>
                <div v-for="skill of Object.entries(Skill['Mobile Development'])" class="skill-content-box-content">
                    {{ skill[1].name }}

                    <Rating :rating="skill[1].rating" />
                </div>

            </div> -->
            <div class="skill-content-box">

                <span>{{ 'Databases' }}</span>
                <div v-for="skill of Object.entries(Skill['Databases'])" class="skill-content-box-content">
                    {{ skill[1].name }}
                    <Rating :rating="skill[1].rating" />
                </div>

            </div>
            <div class="skill-content-box">
                <span>{{ 'Frontend Development' }}</span>
                <div v-for="skill of Object.entries(Skill['Frontend Development'])" class="skill-content-box-content">
                    {{ skill[1].name }}

                    <Rating :rating="skill[1].rating" />
                </div>

            </div>
            <div class="skill-content-box">
                <span>{{ 'Spoken Language' }}</span>
                <div v-for="skill of Object.entries(Skill['Spoken Language'])" class="skill-content-box-content">
                    {{ skill[1].name }}

                    <Rating :rating="skill[1].rating" />
                </div>

            </div>
        </div>
    </div>
</template>

<style scoped>
.skill {
    min-height: 95vh;
    padding: 50px 100px;
    background-color: #100123;
    color: white;
    scroll-margin: 20px;
}

.skill-head {
    font-size: 40px;
    font-weight: 800;
    padding: 50px 0;
    display: flex;
    gap: 50px;
}

.skill-content {
    display: flex;
    flex-wrap: wrap;
    margin-top: 4px;
    justify-content: flex-start;
    gap: 40px;
}

.skill-content-box {
    /* border: 1px solid green; */
    display: flex;
    flex-direction: column;
    width: 500px;
    gap: 10px;
}

.skill-content-box>span {
    font-size: 25px;
    font-weight: 600;
    color: #e896c0;
}

.skill-content-box-content {
    /* color: #e896c0; */
    font-size: 18px;
}
</style>