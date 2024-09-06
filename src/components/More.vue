<script setup>
import MoreCard from "@/components/MoreCard.vue";
</script>

<style scoped>
.main-ctn{
    background: linear-gradient(to bottom, #161616, #000000, #161616);
    color:white;
    padding:8vh 6vw;
}
.title, .desc{
    text-align:center;
}
.title{
    color:#FCA311;
    font-size:38px;
    font-family: "Open Sans", sans-serif;
}
.desc{
    color: #C7C7C7;
    font-family: "Roboto Condensed", system-ui;
}
</style>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <h3 class="title">There is more for you</h3>
            <br>
            <p class="desc">We are unlimited and so are you</p>
            <br>
            <br>
            <MoreCard></MoreCard>
        </div>
    </div>
</template>