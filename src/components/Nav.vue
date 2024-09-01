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
    display:flex;
}
.main-ctn{
    display: flex;
    gap:10px;
}
.m-menu-ctn{
    color:black;
    margin:auto 0;
}
@media screen and (max-width:875px){
    .main-ctn{
        display:none;
    }
}
</style>

<template>
    <div class="ctn">
        <div class="main-ctn">
            <BlueBtn :btnData="loginId"></BlueBtn>
            <BlueBtn :btnData="signUpId"></BlueBtn>
        </div>
        <div class="m-menu-ctn">
            <i class='bx bx-menu'></i>
        </div>
    </div>
</template>