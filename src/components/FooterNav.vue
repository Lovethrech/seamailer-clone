<style scoped>
.main-icon-ctn{

}
.mini-icon-ctn{
    display:flex;
    justify-content:space-between;
    gap:2vw;
}
.pre-icon-ctn{
    margin:auto 0
}
.post-icon-ctn{
    display:flex;
    flex-direction:row;
    gap:2vw;
    background-color:#4f5052;
    color:rgb(255, 252, 252);
    padding: 4px 8px;
    border:3px outset #525253a8;
}
.pre-icon-ctn:active{
    transform: scale(0.5);
    transition: all 2s;
}
</style>

<template>
    <div class="main-icon-ctn">
        <div class="mini-icon-ctn">
            <div class="pre-icon-ctn">
                <i class='bx bxs-navigation' style='color:#ffffff' ></i>
            </div>
            <div class="post-icon-ctn">
                <i class='bx bxs-book' ></i>
                <i class='bx bxl-youtube' ></i>
                <i class='bx bxl-instagram'></i>
                <i class='bx bxl-twitter'></i>
            </div>
        </div>
    </div>
</template>