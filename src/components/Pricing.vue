<script setup>
import PFlash from "@/components/PFlash.vue";
import PCardCtn from "@/components/PCardCtn.vue";
</script>

<style scoped>
.p-ctn{
    display:flex;
    flex-direction: column;
    padding:6vh 0;
    width:100%;
}
.title{
    margin:0 6vw;
    text-align:center;
    font-size:30px;
    font-family: "Open Sans", sans-serif;
}
.desc{
    margin: 0 6vw;
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
            <br>
            <PCardCtn></PCardCtn>
        </div>

        <!-- <i class='bx bxs-book' style='color:#ffffff' ></i> -->
        <!-- <i class='bx bxl-youtube' style='color:#ffffff' ></i> -->
        <!-- <i class='bx bxl-instagram' style='color:#ffffff' ></i> -->
        <!-- <i class='bx bxl-twitter' style='color:#ffffff' ></i> -->
    </div>
</template>