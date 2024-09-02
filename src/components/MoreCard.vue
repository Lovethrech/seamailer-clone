<script setup>
import mores from "@/data/mores.json";
</script>

<style scoped>
.main-ctn{
    display:flex;
    flex-direction:row;
    flex-wrap: wrap;
    justify-content: space-between;
    place-items:center;
    background-color: #252525;
}
.card{
    background-color: #000000;
    margin:3vh 0;
    padding:30px;
    width:300px;
}
.title{
    color:#FCA311;
    font-size:20px;
    font-weight:600;
}
.desc{
    color:#C7C7C7;
    font-size:16px;
}
</style>

<template>
    <div class="main-ctn">
        <div class="card" v-for="more in mores" :key="more.id">
            <p class="title">{{more.title}}</p>
            <br>
            <p class="desc">{{more.desc}}</p>
        </div>
    </div>
</template>