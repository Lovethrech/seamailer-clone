<script setup>
import Chel from "@/components/Chel.vue";
import FooterNav from "@/components/FooterNav.vue";
</script>

<style scoped>
.main-ctn{
    background-color:#000000;
    color:#ffffff;
    padding:1vh 6vw;
}
.mini-ctn{
    display:flex;
    justify-content: space-between;
}
</style>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <Chel></Chel>
            <FooterNav></FooterNav>
        </div>
    </div>
</template>