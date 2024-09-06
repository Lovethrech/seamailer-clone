<script setup>
import {ref} from "vue";
import BlueBtn from "@/components/BlueBtn.vue";
import navLists from "@/data/nav-list.json";

const signUpId = ref([navLists[1]]);
const btnWidth = ref("100%");
</script>

<style scoped>
.main-ctn{
    background-color:#edf2fb;
    padding:6vh 6vw;
    text-align:center;
    color: #14213d;
}
.title{
    font-size:38px;
}
.title b{
    color: #f1914f;
}
.desc{
    font-size:18px;
    font-family: "Roboto Condensed", system-ui;
}
.btn-ctn{
    width:360px;
    margin:0 auto;
}
@media screen and (max-width:700px){
    .btn-ctn{
        width:100%;
    }
}
</style>

<template>
    <div class="main-ctn">
        <div class="mini-ctn">
            <h2 class="title">
                Power your apps and users <br/> with <b>transactional</b> emails
            </h2>
            <br>
            <p class="desc">
                Boost your mobile &amp; web apps with our transactional emails. 
                Get your notification updates emails to your users 100% of the time.
            </p>
            <br/>
            <br/>
            <div class="btn-ctn">
                <BlueBtn 
                    :btnData="signUpId"
                    :btnWidth="btnWidth"
                >
                </BlueBtn>
            </div>
            
        </div>
    </div>
</template>