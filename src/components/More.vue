<script setup>
import MoreCard from "@/components/MoreCard.vue";
</script>

<style scoped>
.main-ctn{
    background: linear-gradient(to bottom, #161616, #000000, #161616);
    color:white;
    padding:6vh 6vw;
}
.title, .desc{
    text-align:center;
}
.title{
    color:#FCA311;
    font-size:30px;
}
.desc{
    color: #C7C7C7;
}
.card-box{
    background-color: transparent;
}
</style>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <h3 class="title">There is more for you</h3>
            <p class="desc">We are unlimited and so are you</p>
            <div class="card-box">
                <MoreCard></MoreCard>
            </div>
        </div>
    </div>
</template>