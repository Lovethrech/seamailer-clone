<script setup>
import Header from "@/components/Header.vue";
import Hero from "@/components/Hero.vue";
import HBottom from "@/components/HBottom.vue";
import GrowthSection from "@/components/GrowthSection.vue";
import MQ from "@/components/MQ.vue";
import More from "@/components/More.vue";
import Pricing from "@/components/Pricing.vue";
</script>

<style scoped>
.pricing{
    display:none;
}
@media screen and (max-width:875px) {
    .pricing{
        display:flex;
    }
}
</style>

<template>
    <div class="ctn">
        <Header></Header>
        <Hero></Hero>
        <HBottom></HBottom>
        <GrowthSection></GrowthSection>
        <MQ></MQ>
        <More></More>
        <Pricing class="pricing"></Pricing>
    </div>
</template>