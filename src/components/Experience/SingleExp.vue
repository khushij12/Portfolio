<script setup>
const props = defineProps(['startDate', 'endDate', 'company', 'role', 'techStack', 'desc'])
</script>

<template>
    <div class="singleExp">
        <div class="circle"></div>
        <div class="duration">{{ props.startDate+"-"+props.endDate }}</div>
        <div class="role">{{ props.role+" at "+props.company }}</div>
        <div class="desc">{{ props.desc }}</div>
    </div>
</template>

<style scoped>
    .singleExp{
        padding: 0 50px;
        display: flex;
        flex-direction: column;
        font-size: 25px;
        gap: 10px;
    }
    .duration{
        color: #c5c5c5d9;
        font-weight: 500;
    }
    .role{
        font-weight: 800;
        color: white;
    }
    .desc{
        font-weight: 400;
        color: #c5c5c5d9;
        font-size: 20px;
    }
</style>