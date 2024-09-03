<script setup>
import {ref} from "vue";
import PCard from "@/components/PCard.vue";
import pricingInfos from "@/data/pricing-infos.json";

const freeId=ref([pricingInfos[0]]);
const freeCardWidth=ref("80%");
</script>

<template>
    <div class="main-ctn">
        <div class="left-chevron-ctn"></div>
        <div class="mini-ctn">
            <PCard 
                :pricingInfo="freeId"
                :cardWidth="freeCardWidth"
            >
            </PCard>
        </div>
        <div class="right-chevron-ctn"></div>
    </div>
</template>