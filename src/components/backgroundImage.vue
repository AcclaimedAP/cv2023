<script>

const background = document.getElementsByClassName('imageContainer');

function followMouse(e) {
  const x = `${(e.clientX * 5) / window.innerWidth}%`;
  const y = `${(e.clientY * 5) / window.innerHeight}%`;

  for (let i = 0; i < background.length; i += 1) {
    background[i].style.left = x;
    background[i].style.top = y;
  }
}
document.addEventListener('mousemove', followMouse);
</script>
<template>
<div class="imageContainer"></div>
</template>
<style scoped lang="scss">
.imageContainer {
  background-image: url('../assets/img/trees-background.jpg');
  position: absolute;
  min-height: 100%;
  min-width: 100%;
  object-fit: cover;
  transform-origin: middle center;
  transform: scale(1.2);
}
</style>
