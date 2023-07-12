<script setup>
import projects from "../../constants/projects";
import Card from "./Card.vue";
import SearchBar from "./Search.vue";

const colors = [[98, 215, 198],[177, 132, 239], [193,153,86], [142,154,79]];
</script>
<script>
export default {
    data(){
        return {
            results:[]
        }
    }
}
</script>
<template>
    <div class="proj">
        <div class="proj-head">
            <p class="proj-head-title">Projects</p>
            <div>
            <!-- <SearchBar /> -->
        </div>
        </div>
        
        <div class="proj-content">
            <div v-for="project in projects" class="proj-content-single">
                <Card :name="project.name" :techStack="project.techStack" :desc="project.desc" :link="project.link" :image-link="project.imageLink" :color="colors[Math.floor(Math.random()*colors.length)]"/>
            </div>
        </div>
    </div>
</template>
<style scoped>
.proj{
    min-height: 95vh;
    padding: 50px 100px;
    background-color: #100123;
    color: white;
    scroll-margin: 20px;
}
.proj-head-title{
    font-size: 40px;
    font-weight: 800;
}
.proj-head {
    
    margin-bottom: 30px;
    display: flex;
    justify-content: space-between;
}
.proj-content{
    display: flex;
    flex-wrap: wrap;
    gap: 50px;
    justify-content: space-around;
}
</style>