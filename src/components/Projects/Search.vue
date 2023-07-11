
<template>
    <div class="search">
        <div class="search-field">
            <input type="search" placeholder="Seach here" class="search-input" v-model="text" />
            <button type="submit" class="search-submit"><i class="bi bi-search"></i></button>
        </div>
        <div class="search-result">
            <div class="select">asasa</div>
            <div class="select">asasa</div>
            <div class="select">asasa</div>
            <div class="select">asasa</div>
            <div class="select">asasa</div>
            <div class="select">asasa</div>
            <div class="select">asasa</div>
            <div class="select">asasa</div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            text: ""
        }
    },
    watch: {
        text() {
            console.log(this.text);
        }
    }
}
</script>
<style scoped>
.select:hover{
    background-color: rgba(0,0,255,0.2);
}
.select{
    padding-left: 10px;
}
.search-result{
    max-width: 280px;
    background-color: white;
    max-height: 100px;
    color: black;
    margin-left: 20px;
    overflow: auto;
    padding: 10px;
}
.search-input {
    width: 300px;
    height: 40px;
    border-top-left-radius: 50px;
    border-bottom-left-radius: 50px;
    padding: 0 12px;
    border: none;
}

.search-input::after {
    border: none;
    outline: none;
}

input[type="search"]::-webkit-search-decoration,
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-results-button,
input[type="search"]::-webkit-search-results-decoration {
    display: none;
}

input[type="search"]:focus {
    outline: none;
    border: none;
}

.search-submit {
    width: 30px;
    height: 40px;
    border-top-right-radius: 50px;
    border-bottom-right-radius: 50px;
    border: none;
}
</style>