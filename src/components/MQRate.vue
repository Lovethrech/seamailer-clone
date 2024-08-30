<script setup>
import { defineProps } from "vue";

const { qRate } = defineProps(['qRate']);

</script>

<template>
    <div class="ctn" :key="qRate[0].id">
        <p class="title">{{qRate[0].title}}</p>
        <p class="desc">{{qRate[0].desc}}</p>
    </div>
</template>