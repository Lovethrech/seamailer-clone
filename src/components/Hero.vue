<script setup>
import HeroText from "@/components/HeroText.vue";
import HeroImg from "@/components/HeroImg.vue";
</script>

<style scoped>
.top-ctn{
    display:flex;
    justify-content:center;
    padding: 8vh 4vw;
}
.main-ctn{

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