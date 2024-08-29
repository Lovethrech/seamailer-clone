<script setup>
import { ref } from "vue";
import Btn from "@/components/Btn.vue";
import navLists from "@/data/nav-list.json";

const loginId = ref([navLists[0]]);
</script>

<style scoped>
.ctn{

}
.main-ctn{

}
</style>

<template>
    <div class="ctn">
        <div class="main-ctn">
            <Btn :btnData="loginId"></Btn>
        </div>
    </div>
</template>