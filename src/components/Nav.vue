<script setup>
import { ref } from "vue";
import BlueBtn from "@/components/BlueBtn.vue";
import MMenu from "@/components/MMenu.vue";
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
.m-menu-icon-ctn{
    color:black;
    margin:auto 0;
    display:none;
}
.m-menu-ctn{
    display:none;
    position:absolute;
    top:6vh;
    right:0;
    left:0;
    width:100%;
    background-color: #14213d;
}
.m-menu-mini-ctn{
    display:flex;
    justify-content: center;
    gap:20vw;
}
@media screen and (max-width:875px){
    .main-ctn{
        display:none;
    }
    .m-menu-icon-ctn{
        display: flex;
        font-size:20px;
    }
}
</style>

<template>
    <div class="ctn">
        <div class="main-ctn">
            <BlueBtn :btnData="loginId"></BlueBtn>
            <BlueBtn :btnData="signUpId"></BlueBtn>
        </div>
        <div class="m-menu-icon-ctn">
            <i class='bx bx-menu'></i>
            <!-- <i class='bx bx-x'></i> -->
        </div>
        <MMenu></MMenu>
    </div>
</template>