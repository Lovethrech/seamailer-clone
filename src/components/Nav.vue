<script setup>
import { ref } from "vue";
import BlueBtn from "@/components/BlueBtn.vue";
import MMenu from "@/components/MMenu.vue";
import navLists from "@/data/nav-list.json";

const loginId = ref([navLists[0]]);
const signUpId = ref([navLists[1]]);
const btnWidth = ref("100%");
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
@media screen and (max-width:875px){
    .main-ctn{
        display:none;
    }
    .m-menu-icon-ctn {
        display: flex;
        font-size: 20px;
    }
}
</style>

<template>
    <div class="ctn">
        <div class="main-ctn">
            <BlueBtn 
                :btnData="loginId"
                :btnWidth="btnWidth"
            >
            </BlueBtn>
            <BlueBtn 
                :btnData="signUpId"
                :btnWidth="btnWidth"
            >
            </BlueBtn>
        </div>
        <div class="m-menu-icon-ctn">
            <i class='bx bx-menu'></i>
            <!-- <i class='bx bx-x'></i> -->
        </div>
        <div class="menu">
            <MMenu></MMenu>  
        </div>
    </div>
</template>