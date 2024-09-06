<script setup>
const {pricingInfo, cardWidth, cardDisplay}=defineProps(['pricingInfo', 'cardWidth', 'cardDisplay']);
</script>

<style scoped>
.card-main-ctn{
    background-color: rgba(160, 155, 155, 0.219);
    padding:9vh 6vw 0;
    margin:0 20px;
    border:10px outset rgba(0, 0, 0, 0.034);
    border-radius:60px 0;
}
.card-mini-ctn{
    font-family: "Roboto Condensed", system-ui;
}
.sups,.subs{
    color:#444444;
    font-size:12px;
}
.name{
    font-size:32px;
    font-weight:700;
}
.list-ctn{
    display:flex;
    flex-direction: row;
    gap:10px;
    margin:10px 0;
}
.list-desc, .list-icon-ctn i{
    display:flex;
    place-items:center;
    text-transform: capitalize;
    font-size:18px;
}
</style>

<template>
    <div class="card-main-ctn" :style="{width:cardWidth, display:cardDisplay}">
        <div class="card-mini-ctn">
            <p class="sups">
                {{ pricingInfo[0].sups }}
            </p>
            <p class="name">
                {{ pricingInfo[0].name }}
            </p>
            <p class="subs">
                {{ pricingInfo[0].subs }}
            </p>
            <br>
            <div class="list-ctn" v-for="pricingList in pricingInfo[0].lists" :key="pricingList.id">
                <div class="list-icon-ctn">
                    <i class='bx bxs-check-circle' ></i>
                </div>
                <p class="list-desc">
                    {{ pricingList.desc}}
                </p>
            </div>
        </div>
    </div>
</template>