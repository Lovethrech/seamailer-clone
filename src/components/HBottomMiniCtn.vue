<script setup>
import converts from "@/data/converts.json";
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
.card:nth-child(2){
    margin-top:2vh;
    margin-bottom: 9vh;
}
.card:nth-child(1), .card:nth-child(3){
    margin:4vh 0 6vh;
}
.title{
    color: #14213d;
    margin-top:2vh;
    font-size:20px;
    font-weight:800;
}
.paragraph{
    color:rgb(110, 110, 110);
    line-height:1.5;
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
.slide{
    background-color: rgb(255, 255, 255);
    width:33.3%;
    height:100%;
    border-radius: 40px;
}
@media screen and (max-width:875px) {
    .slide-ctn{
        display:flex;
    }
    .ctn{
        margin:3vh 0;
        justify-content: left;
        gap:30px;
        width:1200px;
    }
    .card{
        width: 70vw;
    }
    .card:hover{
        transform: scale(1);
    }
    .card:nth-child(2){
        margin-bottom: 0;
    }
    .card:nth-child(1), .card:nth-child(3){
        margin:0;
    }
}
</style>

<template>
    <div class="ctn">
        <div class="card" v-for="convert in converts" :key="convert.id">
            <p class="title">{{convert.title}}</p>
            <br>
            <p class="paragraph">{{convert.paragraph}}</p>
        </div>
    </div>
    <div class="slide-ctn">
        <div class="slide"></div>
    </div>
</template>