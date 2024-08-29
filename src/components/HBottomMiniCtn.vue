<script setup>
import converts from "@/data/converts.json";
</script>

<style scoped>
.ctn{
    display:flex;
    justify-content:center;
    gap:2vw;
    margin-top:8vh;
}
.card{
    width:300px;
    background-color:white;
    border:2px outset #14213d;
    border-radius: 30px;
    padding:30px;
    box-shadow: inset 0px 0px 8px 8px #14213d21;
}
.card:nth-child(2){
    margin:-4vh 0 4vh;
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
</style>

<template>
    <div class="ctn">
        <div class="card" v-for="convert in converts" :key="convert.id">
            <p class="title">{{convert.title}}</p>
            <p class="paragraph">{{convert.paragraph}}</p> 
        </div>
        
    </div>
</template>