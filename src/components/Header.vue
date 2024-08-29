<script setup>
import Logo from "@/components/Logo.vue";
import Nav from "@/components/Nav.vue";
</script>

<style scoped>
.top-ctn{
    position: sticky;
    background-color:rgb(245, 245, 245);
    padding: 1vh 6vw 0;
    border-bottom: 6px outset rgba(255, 255, 255, 0.151);
}
.main-ctn{
    display:flex;
    justify-content: space-between;
}
</style>

<template>
    <div class="top-ctn">
        <div class="main-ctn">
            <Logo></Logo>
            <Nav></Nav>
        </div>
    </div>
</template>