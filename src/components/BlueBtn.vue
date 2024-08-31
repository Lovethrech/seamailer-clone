<script setup>
import { defineProps } from "vue";

const { btnData } = defineProps(['btnData']);
</script>

<style scoped>
.ctn, button{
    border-radius:10px;
    border: 0;
}
.ctn{
    box-shadow:inset 0px 0px 6px 8px black;
}
button{
    width: 100%;
    background-color: #14213d;
    color:white;
    padding:10px 15px;
    text-transform: capitalize;
    font-family: "Roboto Condensed", system-ui;
    font-weight:600;
}
.ctn:hover{
    cursor:pointer;
    transform: scale(0.92);
    transition: all .8s;
}
</style>

<template>
    <div class="ctn">
        <a :href="btnData[0].link " target="_blank" rel="noopener noreferrer">
            <button :key="btnData[0].id">
                {{ btnData[0].name }}
            </button>
        </a>
    </div>
</template>