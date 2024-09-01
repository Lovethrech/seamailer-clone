<script setup>
import BlueBtn from "@/components/BlueBtn.vue";
import navLists from "@/data/nav-list.json";

const loginId = ref([navLists[0]]);
const signUpId = ref([navLists[1]]);

</script>

<template>
    <div class="m-menu-ctn">
        <div class="m-menu-mini-ctn">
            <BlueBtn :btnData="loginId"></BlueBtn>
            <BlueBtn :btnData="signUpId"></BlueBtn>
        </div>
    </div>
</template>