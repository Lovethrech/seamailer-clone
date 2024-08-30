<script setup>
import { ref } from "vue";
import growthInfos from "@/data/growth-infos.json";
import BlueBtn from "@/components/BlueBtn.vue";
import OrangeBtn from "@/components/OrangeBtn.vue";

const btnDescInfo = ref([growthInfos[0]]);
console.log(btnDescInfo);
</script>

<style scoped>
.mini-ctn{
    margin:0 14vw;
}
.card{
    display:flex;
    flex-direction:row;
    justify-content: space-between;
    gap:2vw;
    margin:6vh 0;
}
.card:nth-child(2){
    margin:10vh 0;
    flex-direction:row-reverse;
}
.img-ctn, .img-ctn img{
    border-radius:20px;
}
.img-ctn{
    width:300px;
}
.img-ctn img {
    width: 100%;
}
.title{
    color: #14213d;
    text-transform: capitalize;
    font-size:26px;
    font-weight:600;
}
.desc{
    color:#14213d;
}
.btn-ctn{
    width:130px;
}
</style>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <div class="card">
                <div class="img-ctn">
                    <img :src="growthInfos[0].img" :alt="growthInfos[0].img-alt">
                </div>
                <div class="text-ctn">
                    <p class="title">{{growthInfos[0].title}}</p>
                    <br>
                    <p class="desc">{{growthInfos[0].desc}}</p>
                    <br>
                    <div class="btn-ctn">
                        <BlueBtn :btnData='btnDescInfo'></BlueBtn>
                    </div>
                </div>
            </div>
            <div class="card">
                <div class="img-ctn">
                    <img :src="growthInfos[1].img" :alt="growthInfos[1].img-alt">
                </div>
                <div class="text-ctn">
                    <p class="title">{{growthInfos[1].title}}</p>
                    <br>
                    <p class="desc">{{growthInfos[1].desc}}</p>
                    <br>
                    <div class="btn-ctn">
                        <OrangeBtn :btnData='btnDescInfo'></OrangeBtn>
                    </div>
                </div>
            </div>
            <div class="card">
                <div class="img-ctn">
                    <img :src="growthInfos[2].img" :alt="growthInfos[2].img-alt">
                </div>
                <div class="text-ctn">
                    <p class="title">{{ growthInfos[2].title }}</p>
                    <br>
                    <p class="desc">{{ growthInfos[2].desc }}</p>
                    <br>
                    <div class="btn-ctn">
                        <BlueBtn :btnData='btnDescInfo'></BlueBtn>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>