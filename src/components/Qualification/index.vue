<script setup>
import qualf from "../../constants/qualification.js";
const qualification = qualf[0];
</script>
<template>
    <div class="qual">
        <div class="qual-head">
            <div>EDUCATION</div>
            <div class="qual-head-image"><img src="../../assets/education.png" width="80" height="100"/></div>
        </div>
        <div class="qual-content">
            <div class="qual-duration">{{ qualification.startDate + "-" + qualification.endDate }}</div>
            <div class="qual-qualification">{{ qualification.qualification }}</div>
            <div class="qual-institute">{{ qualification.institute }}</div>
            <div class="qual-grade">{{ qualification.gradeType + " - " + qualification.grade }}</div>
        </div>
    </div>
</template>

<style scoped>
.qual {
    min-height: 95vh;
    padding: 50px 100px;
    background-color: #100123;
    color: white;
    scroll-margin: 20px;
}

.qual-head {
    font-size: 40px;
    font-weight: 800;
    padding: 50px 0;
    display: flex;
    gap: 50px;
}
.qual-content{
    display: flex;
    flex-direction: column;
    gap: 10px;
    font-size: 30px;
}

.qual-duration{
        color: #c5c5c5d9;
        font-weight: 500;
    }
    .qual-institute, .qual-qualification{
        font-weight: 800;
        color: white;
    }

    .qual-institute{
        color: #e896c0;
    }
    .qual-grade{
        font-weight: 400;
        font-size: 20px;
    }
    .qual-head-image{
        position: relative;
        top: -24px;
    }
</style>