<script setup>
import Logo from "@/components/Logo.vue";
import Nav from "@/components/Nav.vue";
</script>

<style scoped>
.ctn{
    padding: 1vh 2vw;
}
.main-ctn{
    display:flex;
}
</style>

<template>
    <div class="ctn">
        <div class="main-ctn">
            <Logo/>
            <Nav/>
        </div>
    </div>
</template>