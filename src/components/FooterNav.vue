<style scoped>
.main-icon-ctn{
    color:#FCA311;
}
.mini-icon-ctn{
    display:flex;
    justify-content:space-between;
    gap:1vw;
}
.mini-icon-ctn i{
    padding:10px;
    border-radius:50%;
    border: 2px dotted #FCA311;
}
.mini-icon-ctn i:hover{
    cursor:pointer;
    background-color: #FCA311;
    color:rgb(0, 0, 0);
    border: 2px inset #fca2114d;
    transform: scale(0.94);
    transition: all .4s;
}
</style>

<template>
    <div class="main-icon-ctn">
        <div class="mini-icon-ctn">
            <i class='bx bxl-youtube' ></i>
            <i class='bx bxl-instagram'></i>
            <i class='bx bxl-twitter'></i>
        </div>
    </div>
</template>