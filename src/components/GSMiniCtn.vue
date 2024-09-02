<script setup>
import { ref } from "vue";
import growthInfos from "@/data/growth-infos.json";
import BlueBtn from "@/components/BlueBtn.vue";
import OrangeBtn from "@/components/OrangeBtn.vue";

const btnDescInfo = ref([growthInfos[0]]);
const textColor = ref("hsl(0, 0%, 100%");
const btnWidth = ref("100%");
</script>

<style scoped>
.card{
    background-color:hsl(0, 0%, 100%);
    display:flex;
    flex-direction:row;
    justify-content: center;
    gap:2vw;
    margin:0vh 0;
    padding:4vh 4vw;
    border:3px outset rgba(0, 0, 0, 0.064);
}
.card:hover{
    transform:scale(0.98);
    transition: all .8s;
}
.card:nth-child(2){
    flex-direction:row-reverse;
    margin: 8vh 0;
}
.img-ctn, .img-ctn img{
    border-radius:20px;
}
.img-ctn{
    width:400px;
    display:flex;
    justify-content: right;
}
.img-ctn img {
    width: 100%;
}
.title{
    color: #14213d;
    text-transform: capitalize;
    font-size:22px;
    font-family: "Open Sans", sans-serif;
    font-weight:600;
}
.desc{
    color:#14213d;
    width:400px;
    line-height: 1.5;
    font-size:16px;
    font-family: "Roboto Condensed", system-ui;
}
.btn-ctn{
    width:130px;
}
@media screen and (max-width:875px){
    .desc{
        font-size:14px;
    }
    .card:hover{
        transform:scale(1);
    }
}
@media screen and (max-width:780px) {
    .card, .card:nth-child(2){
        justify-content: center;
        place-items:center;
    }
    .card{
        flex-direction:column;
    }
    .card:nth-child(2){
        flex-direction: column;
    }
}
@media screen and (max-width:600px) {
    .img-ctn, .desc{
        width:100%;
    }
    .desc{
        text-align:justify;
    }
}
</style>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <div class="card">
                <div class="img-ctn">
                    <img :src="growthInfos[0].img" :alt="growthInfos[0].imgAlt">
                </div>
                <div class="text-ctn">
                    <p class="title">{{growthInfos[0].title}}</p>
                    <br>
                    <p class="desc">{{growthInfos[0].desc}}</p>
                    <br>
                    <div class="btn-ctn">
                        <BlueBtn :btnWidth="btnWidth" :btnData='btnDescInfo'></BlueBtn>
                    </div>
                </div>
            </div>
            <div class="card">
                <div class="img-ctn">
                    <img :src="growthInfos[1].img" :alt="growthInfos[1].imgAlt">
                </div>
                <div class="text-ctn">
                    <p class="title">{{growthInfos[1].title}}</p>
                    <br>
                    <p class="desc">{{growthInfos[1].desc}}</p>
                    <br>
                    <div class="btn-ctn">
                        <OrangeBtn :textColor="textColor" :btnData='btnDescInfo'></OrangeBtn>
                    </div>
                </div>
            </div>
            <div class="card">
                <div class="img-ctn">
                    <img :src="growthInfos[2].img" :alt="growthInfos[2].imgAlt">
                </div>
                <div class="text-ctn">
                    <p class="title">{{ growthInfos[2].title }}</p>
                    <br>
                    <p class="desc">{{ growthInfos[2].desc }}</p>
                    <br>
                    <div class="btn-ctn">
                        <BlueBtn :btnWidth="btnWidth" :btnData='btnDescInfo'></BlueBtn>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>