<script setup>
const { qRate } = defineProps(['qRate']);
</script>

<style scoped>
.ctn{
    margin:3vh 0;
}
.title{
    color:white;
    font-family: "Bebas Neue", sans-serif;
    font-weight:600;
    font-size:30px;
    letter-spacing:2px;
}
p{
    color: #C7C7C7;
    font-family: "Roboto Condensed", system-ui;
}
</style>

<template>
    <div class="ctn" :key="qRate[0].id">
        <p class="title">{{qRate[0].title}}</p>
        <br/>
        <p class="desc">{{qRate[0].desc}}</p>
    </div>
</template>