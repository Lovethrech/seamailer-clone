<script setup>
import GSMiniCtn from "@/components/GSMiniCtn.vue";
</script>

<style scoped>
.main-ctn{
    padding:8vh 6vw 4vh;
}
h2, p{
    text-align:center;
    color:#14213d;
    line-height:1.5;
}
h2{
    font-size:30px;
    font-family: "Open Sans", sans-serif;
    font-weight:600;
}
p{
    font-size:16px;
    font-family: "Roboto Condensed", system-ui;
}
@media screen and (max-width:875px) {
    h2{
        font-size:24px;
    }
    p{
        font-size:14px;
    }
}
</style>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <h2>
                Made for your growth
            </h2>
            <br>
            <p>
                We have built and tailored Seamailer for your work to achieve more when talking to your customers
            </p>
            <GSMiniCtn></GSMiniCtn>
        </div>
    </div>
</template>