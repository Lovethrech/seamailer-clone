<script setup>
import {ref} from "vue";
import PCard from "@/components/PCard.vue";
import pricingInfos from "@/data/pricing-infos.json";

const freeId=ref([pricingInfos[0]]);
const creatorId=ref([pricingInfos[1]]);
const professionalId=ref([pricingInfos[2]]);
const freeDisplay=ref("flex");
const creatorDisplay=ref("none");
const professionalDisplay=ref("none");
const freeCardWidth=ref("90vw");
const displayLeftIcon=ref("none");
const displayRightIcon=ref("flex");

const togglePriceRight=()=>{
    if (freeDisplay.value==="flex"){
        freeDisplay.value="none";
        creatorDisplay.value="flex";
        professionalDisplay.value="none";
        displayLeftIcon.value="flex";
        displayRightIcon.value="flex";
    }
    else if (creatorDisplay.value==="flex"){
        freeDisplay.value="none";
        creatorDisplay.value="none";
        professionalDisplay.value="flex";
        displayLeftIcon.value="flex";
        displayRightIcon.value="none";
    }
    else{
        freeDisplay.value="flex";
        creatorDisplay.value="none";
        professionalDisplay.value="none";
        displayLeftIcon.value="none";
        displayRightIcon.value="flex";
    }
}
const togglePriceLeft=()=>{
    if (creatorDisplay.value==="flex"){
        freeDisplay.value="flex";
        creatorDisplay.value="none";
        professionalDisplay.value="none";
        displayLeftIcon.value="none";
    }
    else if (professionalDisplay.value==="flex"){
        freeDisplay.value="none";
        creatorDisplay.value="flex";
        professionalDisplay.value="none";
        displayLeftIcon.value="flex";
        displayRightIcon.value="flex";
    }
    else{
        freeDisplay.value="flex";
        creatorDisplay.value="none";
        professionalDisplay.value="none";
        displayLeftIcon.value="none";
        displayRightIcon.value="flex";
    }
}
</script>

<style scoped>
.main-ctn{
    display:flex;
    flex-direction:row;
    justify-content: space-between;
    gap:10px;
    width:3200px;
}
.mini-ctn{
    display:flex;
    flex-direction:row;
    
}
.left-chevron-ctn, .right-chevron-ctn{
    position:absolute;
    display:flex;
    justify-content: center;
    place-items:center;
    background-color: rgba(0, 0, 0, 0.397);
    font-size:40px;
    width:50px;
}
.left-chevron-ctn{
    left:0;
    margin-top:200px;
    border-radius: 0 20px 20px 0;
}
.right-chevron-ctn{
    right:0;
    margin-top:200px;
    border-radius:20px 0 0 20px;
}
</style>

<template>
    <div>
        <div class="main-ctn">
            <div :onClick="togglePriceLeft" class="left-chevron-ctn" >
                <i class='bx bxs-chevron-left' :style="{display:displayLeftIcon}"></i>
            </div>
            <div class="mini-ctn">
                <PCard 
                    :pricingInfo="freeId"
                    :cardDisplay="freeDisplay"
                    :cardWidth="freeCardWidth"
                >
                </PCard>
                <PCard 
                    :pricingInfo="creatorId"
                    :cardDisplay="creatorDisplay"
                    :cardWidth="freeCardWidth"
                >
                </PCard>
                <PCard 
                    :pricingInfo="professionalId"
                    :cardDisplay="professionalDisplay"
                    :cardWidth="freeCardWidth"
                >
                </PCard>
            </div>
            <div :onClick="togglePriceRight" class="right-chevron-ctn">
                <i class='bx bxs-chevron-right'  :style="{display:displayRightIcon}"></i>
            </div>
        </div>
    </div>
</template>