<script setup>
import { ref } from "vue";
import MQRate from "@/components/MQRate.vue";
import growthInfos from "@/data/growth-infos.json";
import qRates from "@/data/q-rates.json";
import OrangeBtn from "@/components/OrangeBtn.vue";

const btnDescInfo = ref([growthInfos[0]]);
const typeId = ref([qRates[0]]);
const deliverId = ref([qRates[1]]);
const supportId = ref([qRates[2]]);
const textColor = ref("hsl(0, 0%, 0%");
</script>

<style scoped>
.main-ctn{
    background-color:#14213d;
    color:white;
    display:flex;
    justify-content: center;
    padding:4vh 4vw;
}
h3{
    color:#C7C7C7;
    font-family: "Roboto Condensed", system-ui;
    text-align:center;
    font-size:36px;
}
.logo-name{
    color:#FCA311;
}
.rate{
    margin:4vh 0;
    display:flex;
    flex-direction: row;
    justify-content: center;
    gap:6vw;
    text-align:center;
}
@media screen and (max-width:875px) {
    .rate{
        flex-direction:column;
    }
}
</style>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <h3>Why choose <b class="logo-name">Seamailer?</b></h3>
            <div class="rate">
                <MQRate :qRate="typeId"></MQRate>
                <MQRate :qRate="deliverId"></MQRate>
                <MQRate :qRate="supportId"></MQRate>
            </div>
            <OrangeBtn :textColor="textColor" :btnData='btnDescInfo'></OrangeBtn>
            <p class="btn-text"></p>
        </div>
    </div>
</template>