<script setup>
</script>
<template>
<div class="container"><div class="color"></div></div>
</template>

<style scoped lang="scss">
.container {

    min-height: 50px;
    max-height: 50px;
    width: 50%;
    transform: translateX(50%);
    left: -50%;
    transform-origin: left center;
    position: relative;

    &:hover > .color{
        transform: translateX(0);
        transition: all 0.2s ease-out;
    }

}
.color {
    box-shadow: 0px 0px 5px rgb(199, 158, 71);
    position: absolute;
    right: 0;
    transition: transform 2s ease-in-out;
    transform: translateX(-30%);
    //background-color: $green-pastel;
    background-color: rgb(199, 158, 71);
    min-width: 20%;
    height: 100%;
    max-height: 3px;
}
</style>
