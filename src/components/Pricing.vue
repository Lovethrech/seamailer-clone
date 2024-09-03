<script setup>
import PFlash from "@/components/PFlash.vue";
</script>

<style scoped>
.p-ctn{
    display:flex;
    flex-direction: column;
    padding:6vh 6vw;
}
.p-mini-ctn{

}
.title{
    text-align:center;
    font-size:30px;
    font-family: "Open Sans", sans-serif;
}
.desc{
    text-align:center;
    color:#636262;
    font-size:16px;
    font-family: "Roboto Condensed", system-ui;
}
</style>

<template>
    <div class="p-ctn">
        <PFlash></PFlash>
        <br>
        <div class="p-mini-ctn">
            <h3 class="title">Pricing tailored to your usage</h3>
            <p class="desc">You only pay for what you use, no hidden charges.</p>
        </div>
    </div>
</template>