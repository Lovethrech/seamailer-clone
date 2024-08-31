<script setup>
import { ref } from "vue";
import converts from "@/data/converts.json";

// Getting a timed-slider
const scrollOneColor = ref("hsl(0, 0%, 100%)");
const scrollTwoColor = ref("transparent");
const scrollThreeColor = ref("transparent");
const windowWidth = ref(window.innerWidth);
const slideOneStyleMargin = ref('4vh 0 4vh');
const slideTwoStyleMargin = ref('2vh 0 4vh');
const slideThreeStyleMargin = ref('4vh 0 4vh');

function updateStyles() {
    if (windowWidth.value < 875) {
        slideOneStyleMargin.value = '4vh 0 4vh';
        slideTwoStyleMargin.value = '2vh 0 4vh';
        slideThreeStyleMargin.value = '4vh 0 4vh'; 
    }
    else {
        setInterval(() => {
            if (scrollOneColor.value === "hsl(0,0%,100%)") {
                scrollOneColor.value = "transparent";
                scrollTwoColor.value = "hsl(0, 0%, 100%)";
                scrollThreeColor.value = "transparent";
                slideOneStyleMargin.value = '0 0 0 -8vw';
                slideTwoStyleMargin.value = '0';
                slideThreeStyleMargin.value = '0';
            }
            else if (scrollTwoColor.value === "hsl(0, 0%, 100%)") {
                scrollOneColor.value = "transparent";
                scrollThreeColor.value = "hsl(0, 0%, 100%)";
                scrollTwoColor.value = "transparent";
                scrollThreeColor.value = "hsl(0, 0%, 100%)";
                slideOneStyleMargin.value = '0 0 0 -330vw';
                slideTwoStyleMargin.value = '0';
                slideThreeStyleMargin.value = '0';
            }
            else {
                scrollTwoColor.value = "transparent";
                scrollOneColor.value = "hsl(0, 0%, 100%)";
                scrollThreeColor.value = "transparent";
                slideOneStyleMargin.value = '0 0 0 -700vw';
                slideTwoStyleMargin.value = '0';
                slideThreeStyleMargin.value = '0';
            }
        }, 5000); 
    }
}

window.addEventListener('resize', () => {
    windowWidth.value = window.innerWidth;
    updateStyles();
})
</script>

<style scoped>
.ctn{
    display:flex;
    justify-content:center;
    gap:2vw;
    margin:4vh 0 3vh;
}
.card{
    width:350px;
    background-color:white;
    border:1px outset #14213d;
    border-radius: 30px;
    padding:30px;
    box-shadow: inset 0px 0px 8px 8px #14213d21;
}
.card:hover{
    transform: scale(1.05);
    transition: all 1s;
}
.title{
    color: #14213d;
    margin-top:2vh;
    font-size:20px;
    font-family: "Open Sans", sans-serif;
    font-weight:600;
}
.paragraph{
    color:rgb(110, 110, 110);
    line-height:1.5;
    font-family: "Roboto Condensed", system-ui;
}
.slide-ctn{
    display:none;
    background-color: rgba(0, 0, 0, 0.479);
    width:50%;
    height:2px;
    margin: 0 auto;
    border-radius:40px;
    box-shadow: 0px 0px 1px 1px rgba(0, 0, 0, 0.219);
}
.scroll-one, .scroll-two, .scroll-three{
    width:33%;
    height:100%;
    border-radius: 40px;
}
@media screen and (max-width:875px) {
    .slide-ctn{
        display:flex;
        justify-content: space-between;
    }
    .ctn{
        margin:3vh 0;
        justify-content: left;
        gap:30px;
        width:300vw;
    }
    .card{
        width: 70vw;
        transition: all 1s;
    }
    .card:hover{
        transform: scale(1);
    }
}
</style>

<template>
    <div class="ctn">
        <div class="card" :style="{margin: slideOneStyleMargin}">
            <p class="title">{{converts[0].title}}</p>
            <br>
            <p class="paragraph">{{converts[0].paragraph}}</p>
        </div>
        <div class="card" :style="{margin: slideTwoStyleMargin}">
            <p class="title">{{converts[1].title}}</p>
            <br>
            <p class="paragraph">{{converts[1].paragraph}}</p>
        </div>
        <div class="card" :style="{margin: slideThreeStyleMargin}">
            <p class="title">{{converts[2].title}}</p>
            <br>
            <p class="paragraph">{{converts[2].paragraph}}</p>
        </div>

    </div>
    <div class="slide-ctn">
        <div :style="{ backgroundColor: scrollOneColor }" class="scroll-one"></div>
        <div :style="{ backgroundColor: scrollTwoColor }" class="scroll-two"></div>
        <div :style="{ backgroundColor: scrollThreeColor }" class="scroll-three"></div>
    </div>
</template>