<script setup>
import { ref } from "vue";
import BlueBtn from "@/components/BlueBtn.vue";
import navLists from "@/data/nav-list.json";

const loginId = ref([navLists[0]]);
const signUpId = ref([navLists[1]]);
</script>

<style scoped>
.ctn{
    margin:auto 0;
}
.main-ctn{
    display: flex;
    gap:10px;
}
</style>

<template>
    <div class="ctn">
        <div class="main-ctn">
            <BlueBtn :btnData="loginId"></BlueBtn>
            <BlueBtn :btnData="signUpId"></BlueBtn>
        </div>
    </div>
</template>