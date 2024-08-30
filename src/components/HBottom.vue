<script setup>
import HBottomMiniCtn from "@/components/HBottomMiniCtn.vue";
</script>

<style scoped>
.main-ctn{
    background-color:#edf2fb;
    padding:4vh 6vw;
}
h2{
    text-align:center;
    color: #14213d;
    font-size:30px;
    font-weight:600;
}
@media screen and (max-width:875px) {
    h2{
        font-size:26px;
    }
}
</style>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <h2>
                Send marketing emails that converts contacts into customers
            </h2>
            <HBottomMiniCtn></HBottomMiniCtn>
        </div>
    </div>
</template>