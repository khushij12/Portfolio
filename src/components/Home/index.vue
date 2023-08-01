<template>
    <div class="main">
        <div class="intro"><span class="heading"><b>Greetings and welcome to my portfolio! <br>Hi! I'm Khushi
                    Jain</b>.</span><br>
            <b style="font-size: 20px;">Frontend and backend developer? Oh, I've got both areas covered like a boss!</b>
        </div>
        <div class="dummy"><img src="../../assets/F!.png" width="120" height="160" /></div>
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

@keyframes entry {
    0% {
        transform: translate(-400px);
    }
}

.intro {
    flex-basis: content;
    animation: entry 1s ease-in 1;
}

.heading {
    font-size: 30px;
    color: #e896c0;
}

@keyframes dummyEntry {
    0% {
        transform: translateY(-300px);
    }

    100% {
        transform: translateY(0);
    }
}

@keyframes jump {
    0% {
        bottom: 0;
    }

    50% {
        bottom: 50px;
    }

    100% {
        bottom: 0;
    }
}

.dummy {
    position: relative;
    animation: dummyEntry 0.9s ease-in 1, jump 1.1s ease-out infinite;
}
</style>