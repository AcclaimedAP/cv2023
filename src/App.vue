<script setup>
// import content from './components/ContextText.vue';
import circleShimmer from './components/circleShimmer.vue';

const background = document.getElementsByClassName('imageContainer');

document.onmousemove = function followMouse() {
  const x = `${(event.clientX * 5) / window.innerWidth}%`;
  const y = `${(event.clientY * 5) / window.innerHeight}%`;

  for (let i = 0; i < 2; i += 1) {
    background[i].style.left = x;
    background[i].style.top = y;
  }
};
</script>

<template>
  <div class="background">
    <div class="imageContainer"></div>
  <circleShimmer class="circleShimmer" />
  </div>
</template>

<style scoped lang="scss">
.background {

  position: fixed;
  height: 100vh;
  width: 100vw;
  margin: 0;
}
.imageContainer {
  background-image: url('assets/img/trees-background.jpg');
  position: absolute;
  min-height: 100%;
  min-width: 100%;
  object-fit: cover;
  transform-origin: middle center;
  transform: scale(1.2);
}
.circleShimmer {
  margin: auto;
}
</style>
