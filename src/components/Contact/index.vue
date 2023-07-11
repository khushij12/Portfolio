<script setup>
import links from "../../constants/links";
</script>
<template>
    <div class="contact">
        <div class="contact-head">
            Let's connect
        </div>
        <div class="as">
        <div class="contact-body">

            <div v-for="link in links" class="contact-content">
                <a :href="link.url" target="_blank"><img :src="link.logo" /></a>
            </div>
            
        </div>
        <!-- <div class="asd">
            <img src="../../assets/F2.png" width="180" height="280"/>
        </div> -->
    </div>
    </div>
</template>
<style scoped>
.contact {
    min-height: 85vh;
    padding: 50px 100px;
    background-color: #100123;
    color: white;
    scroll-margin: 20px;
}

.contact-head {
    font-size: 40px;
    font-weight: 800;
    margin-bottom: 30px;
}

.contact-content {
    width: 72px;
    height: 72px;
    background-color: #FFF;
    fill: linear-gradient(0deg, #FFF 0%, #FFF 100%), #272727;
    filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
    border-radius: 25px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.contact-content:hover {
    fill: linear-gradient(0deg, #FFF 0%, #FFF 100%), #272727;
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25) inset;
    filter: none;
}

a {
    background-color: white;
    text-decoration: none;
}

a::after {
    background-color: white;
    text-decoration: none;
}

/* .contact-content: {

} */
.contact-body {
    padding: 40px 20px;
    display: flex;
    gap: 57px;
    justify-content: flex-start;
    flex-wrap: wrap;
    margin-top: 50px;
    width: 245px;
    height: 300px;
    border-radius: 25px;
    background: #FFF;
background: rgba(255, 255, 255, 0.2);
box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
backdrop-filter: blur(5px);
-webkit-backdrop-filter: blur(5px);
/* border: 1px solid rgba(255, 255, 255, 0.3); */
}
.asd{
    padding: 40px 20px;
}
.as{
    display: flex;
    flex-direction: row;
    gap: 450px;
}
</style>