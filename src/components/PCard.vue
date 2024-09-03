<script setup>
const {pricingInfo, cardWidth}=defineProps(['pricingInfo', 'cardWidth']);
</script>

<style scoped>
.card-main-ctn{
    background-color: white;
    padding:20px;
}
.card-mini-ctn{
    font-family: "Roboto Condensed", system-ui;
}
.sups,.subs{
    color:#444444;
    font-size:14px;
}
.name{
    font-size:28px;
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
    font-size:16px;
}
</style>

<template>
    <div class="card-main-ctn" :style="{width:cardWidth}">
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