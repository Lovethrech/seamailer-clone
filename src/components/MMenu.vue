<script setup>
import { ref } from "vue";
import BlueBtn from "@/components/BlueBtn.vue";
import navLists from "@/data/nav-list.json";

const loginId = ref([navLists[0]]);
const signUpId = ref([navLists[1]]);
const loginBtnWidth = ref("300px");
const signUpBtnWidth = ref("100px");
</script>
<style scoped>
.m-menu-ctn {
    position: absolute;
    top: 6vh;
    right: 0;
    left: 0;
    width: 100%;
    background-color: #ffffff;
    padding:20px 6vw;
}
.m-menu-mini-ctn {
    display: flex;
    justify-content: center;
    gap: 2vw;
}
@media screen and (max-width:875px) {
    .m-menu-icon-ctn {
        display: flex;
        font-size: 20px;
    }
}
</style>

<template>
    <div class="m-menu-ctn">
        <div class="m-menu-mini-ctn">
            <BlueBtn 
                :btnData="loginId"
                :btnWidth="loginBtnWidth"
            >
            </BlueBtn>
            <BlueBtn 
                :btnData="signUpId"
                :btnWidth="signUpBtnWidth"
            >
            </BlueBtn>
        </div>
    </div>
</template>