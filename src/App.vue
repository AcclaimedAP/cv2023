<script setup>
// import content from './components/ContextText.vue';
import circleShimmer from './components/circleShimmer.vue';
import background from './components/backgroundImage.vue';
import navbar from './components/navbarLandingpage.vue';

function test(x) {
  console.log(x);
}
</script>

<template>
  <div class="background">
    <background />
    <navbar @location="test"/>
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

.circleShimmer {
  margin: auto;
}
</style>
