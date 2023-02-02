<script>

export default {
    props: {
        name: String,
        info: String,
        icon: String,
        alt: String
    },
    data() {
        return {
            imageAttributes: {
                src: this.icon,
                alt: this.alt
            }
        }
    }
}
</script>

<template>
<details>
    <summary><img v-if="icon" v-bind="imageAttributes" />{{ name }}</summary>
    <p>{{ info }}</p>
</details>
</template>

<style scoped lang="scss">
@keyframes details-show {
  0% {
    margin-bottom: -30%;
    opacity: 0;

  } 100% {
    margin-bottom: 0;
    opacity: 1;

  }
}
details {
    background-color: rgba($white, 0.05);
    text-align: center;
    overflow: hidden;
    height: auto;
    z-index: 1;
    line-height: 36px;
    p {
        margin: 0;
    }

    
    summary {
        list-style: none;
        background-color: rgba($white, 0.03);
        display: block;
        z-index: 10;
        position: relative;
        cursor: pointer;
        &::before {

        }
        &::after {
            content: '';
            border-right: 4px solid;
            border-bottom: 4px solid;
            position: absolute;
            top: 8px;
            right: 20px;
            height: 10px;
            width: 10px;
            transform: rotate(45deg);
            transition: all 0.4s;
            
        }
            
        &:hover {
            background-color: rgba($white, 0.1);
        }
    }
}
details[open] > summary::after {
  transform: rotate(-135deg);
}
details > *:not(summary) {
  animation: details-show 1s ease-in-out;
  position: relative;
  z-index: 1;
  transition: all 0.3s ease-in-out;
  color: transparent;
  overflow: hidden;
}
details[open] > *:not(summary) { color: inherit; }
</style>