<style scoped>
.ctn{
    display:flex;
    justify-content:center;
}
.main-ctn{
    display:flex;
    justify-content: center;
    width:50vw;
    height:30vw;
    margin-top:3vh;
    background: linear-gradient(to right, #f2b870, #f1914f);
    padding:3vh 3vw;
    box-shadow: inset 0px 0px 8px 8px #8a6a4480;
}
.ctn img{
    width:40vw;
}
@media screen and (max-width:875px) {
    .main-ctn{
        width:80vw;
        height:50vw;
    }
    .ctn img{
        width:70vw;
    }
}
</style>

<template>
    <div class="ctn">
        <div class="main-ctn">
            <img src="/Hero.png" alt="">  
        </div>
    </div>
</template>