<script setup>
import { ref } from "vue";
import BlueBtn from "@/components/BlueBtn.vue";
import MMenu from "@/components/MMenu.vue";
import navLists from "@/data/nav-list.json";

const loginId = ref([navLists[0]]);
const signUpId = ref([navLists[1]]);
const btnWidth = ref("100%");
const menuIcon = ref("<i class='bx bx-menu'></i>");
const showDropdown = ref(false);
const displayMenu = () => {
    if (showDropdown.value === false) {
        menuIcon.value = "<i class='bx bx-x'></i>";
        showDropdown.value = true;
    }
    else {
        menuIcon.value = "<i class='bx bx-menu'></i>";
        showDropdown.value = false;
    }
}
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
        <div 
            :onClick="displayMenu"
            v-html="menuIcon"
            class="m-menu-icon-ctn" 
        >
        </div>
        <div v-show="showDropdown" class="menu">
            <MMenu></MMenu>  
        </div>
    </div>
</template>