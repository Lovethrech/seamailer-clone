<script setup>
import mores from "@/data/mores.json";
</script>

<style scoped>
.main-ctn-mini{
    background: transparent;
    display:flex;
    flex-direction:row;
    flex-wrap: wrap;
    justify-content: center;
    place-items:center;
    gap:4vw;
}
.card{
    background-color: #000000;
    margin:3vh 0;
    padding:30px;
    width: 400px;
    height:220px;
    min-width:100px;
    box-shadow: inset -4px -4px 8px 8px rgba(32, 32, 32, 0.336);
}
.title{
    color:#FCA311;
    font-size:22px;
    font-weight:600;
    font-family: "Open Sans", sans-serif;
}
.desc{
    color:#C7C7C7;
    font-size:16px;
    line-height: 1.5;
    font-family: "Roboto Condensed", system-ui;
}
.card:nth-child(2) .title, .card:nth-child(4) .title, .card:nth-child(6) .title, .card:nth-child(8) .title{
    color:#70D6ff;
}

@media screen and (max-width:800px) {
    .card{
        width:90%;
        height:100%;
    }
}
</style>

<template>
    <div class="main-ctn-mini">
        <div class="card" v-for="more in mores" :key="more.id">
            <h2 class="title">{{more.title}}</h2>
            <br>
            <p class="desc">{{more.desc}}</p>
        </div>
    </div>
</template>