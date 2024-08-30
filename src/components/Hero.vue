<script setup>
import HeroText from "@/components/HeroText.vue";
import HeroImg from "@/components/HeroImg.vue";
</script>

<style scoped>
.top-ctn{
    display:flex;
    justify-content:center;
    padding: 8vw 6vw 10vw;
}
</style>

<template>
    <div class="top-ctn">
        <div class="main-ctn">
            <HeroText></HeroText>
            <HeroImg></HeroImg>
        </div>
    </div>
</template>