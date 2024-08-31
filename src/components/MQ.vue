<script setup>
import { ref } from "vue";
import MQRate from "@/components/MQRate.vue";
import qRates from "@/data/q-rates.json";

const typeId = ref([qRates[0]]);
const deliverId = ref([qRates[1]]);
const supportId = ref([qRates[2]]);
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
                <br/>
                <MQRate :qRate="deliverId"></MQRate>
                <br/>
                <MQRate :qRate="supportId"></MQRate>
            </div>
        </div>
    </div>
</template>