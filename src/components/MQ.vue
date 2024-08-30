<script setup>
import { ref } from "vue";
import MQRate from "@/components/MQRate.vue";
import qRates from "@/data/q-rates.json";

const typeId = ref([qRates[0]]);
const deliverId = ref([qRates[1]]);
const supportId = ref([qRates[2]]);
</script>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <h3>Why choose <b class="logo-name">Seamailer?</b></h3>
            <div class="rate">
                <MQRate :qRate="typeId"></MQRate>
            </div>
            
        </div>
    </div>
</template>