<script setup>
import { defineProps } from "vue";

const { btnData } = defineProps(['btnData']);
console.log(btnData[0].name);
</script>

<template>
    <div class="ctn">
        <a :href="btnData[0].link " target="_blank" rel="noopener noreferrer">
            <button :key="btnData[0].id" class="login">
                {{ btnData[0].name }}
            </button>
        </a>
    </div>
</template>