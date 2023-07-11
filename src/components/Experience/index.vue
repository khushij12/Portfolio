<script setup>
import SingleExp from './SingleExp.vue';
import constants from "../../constants/experience";

</script>
<template>
    <div class="exp">
        <p class="exp-head">WORK EXPERIECNCE</p>
        <div v-for="item in constants" class="exp-box">
            <div class="circle"></div>
            <SingleExp :start-date="item.startDate" :end-date="item.endDate" :company="item.company" :role="item.role"
                :tech-stack="item.techStack" :desc="item.desc" />
        </div>

    </div>
</template>

<style scoped>
.exp {
    min-height: 95vh;
    padding: 50px 100px;
    background-color: #100123;
    color: white;
    scroll-margin: 20px;
}

.exp-head {
    font-size: 40px;
    font-weight: 800;
    margin-bottom: 30px;
}

.exp-box {
    border-left: 0.5px solid #e896c0;
    /* border-top: 0.5px solid #e896c0; */
    display: flex;
    padding-bottom: 20px;
}

div.exp-box :first-child {
    padding-top: 0;
    border-right: 1px solid #e896c0;
}

.circle {
    border-radius: 50%;
    width: 12px;
    height: 12px;
    background-color: #e896c0;
    position: relative;
    /* top: 10px; */
    left: -6px;
    flex-shrink: 0;
}
</style>