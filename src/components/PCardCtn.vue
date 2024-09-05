<script setup>
import {ref} from "vue";
import PCard from "@/components/PCard.vue";
import pricingInfos from "@/data/pricing-infos.json";

const freeId=ref([pricingInfos[0]]);
const freeCardWidth=ref("90vw");
const displayLeftIcon=ref("none");

const togglePriceRight=()=>{
    if (freeId.value==[pricingInfos[0]]){
        freeId.value=[pricingInfos[1]];
        displayLeftIcon.value="flex";
    }
}
</script>

<style scoped>
.main-ctn{
    display:flex;
    flex-direction:row;
    justify-content: space-between;
    gap:10px;
}
.left-chevron-ctn, .right-chevron-ctn{
    display:flex;
    justify-content: center;
    place-items:center;
    font-size:40px;
    width:50px;
}
</style>

<template>
    <div class="main-ctn">
        <div class="left-chevron-ctn" >
            <i class='bx bxs-chevron-left' :style="{display:displayLeftIcon}"></i>
        </div>
        <div class="mini-ctn">
            <PCard 
                :pricingInfo="freeId"
                :cardWidth="freeCardWidth"
            >
            </PCard>
        </div>
        <div :onClick="togglePriceRight" class="right-chevron-ctn">
            <i class='bx bxs-chevron-right' style='color:#000000' ></i>
        </div>
    </div>
</template>