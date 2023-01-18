<script>
import lines from './shimmerLine.vue';

export default {
  components: {
    lines,
  },
  data() {
    return {
      amount: 72,
    };
  },

};
</script>

<template>

<div><lines v-for="count in amount" :key="`component-${count}`" class="lines"/></div>

</template>

<style scoped lang="scss">
@keyframes fadeIn{
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}
div {
    animation: 3s ease-out 0s 1 fadeIn;
    transition: all 1s ease-out;
    width: 100vh;
    height: 100vh;
    background-color: rgb(30, 30, 130, 0);
    margin: 0;
    position: relative;
    @for $i from 1 through 72 {
        .lines:nth-child(#{$i}){
            transform: rotate(calc(5deg * $i));
        }
    }
    .lines {
        position: absolute;
        top: 50%;
        left: 50%;
    }
}
</style>
