<script setup>
import { ref } from "vue";
import growthInfos from "@/data/growth-infos.json";
import BlueBtn from "@/components/BlueBtn.vue";
import OrangeBtn from "@/components/OrangeBtn.vue";

const btnDescInfo = ref([growthInfos[0]]);
console.log(btnDescInfo);
</script>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <div class="card" v-for="growthInfo in growthInfos" :key="growthInfo.id">
                <div class="img-ctn">
                    <img :src="growthInfo.img" :alt="growthInfo.img-alt">
                </div>
                <div class="text-ctn">
                    <p class="title">{{growthInfo.title}}</p>
                    <p class="desc">{{growthInfo.desc}}</p>
                    <div :v-html="growthInfo.btn" class="btn-ctn"></div>
                </div>
            </div>

        </div>
    </div>
</template>