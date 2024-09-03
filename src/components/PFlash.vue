<style scoped>
.ctn{
    display:flex;
    justify-content: center;
    place-items:center;
    width:100%;
}
.mini-ctn{
    display:flex;
    justify-content: center;
    gap:10px;
    font-size:12px;
    background-color:rgba(0, 128, 0, 0.13);
    color:green;
    padding:5px 10px;
    border-radius:20px;
    border:2px solid green;
}
.mini-ctn:hover{
    transform:scaleX(1.04);
    transition: all 1s;
}
</style>

<template>
    <div class="ctn">
        <div class="mini-ctn">
            <div class="icon-ctn">
                <i class='bx bxs-zap'></i>
            </div>
            <p>Set sail with our price</p>
        </div>
    </div>
</template>