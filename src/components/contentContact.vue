<script>
import content from './titleTextLinkComponent.vue';

export default {
    components: {
        content,
    }
}
</script>

<template>
<div class="container">
<h1>Projekt</h1>

<content title="Test title" 
text="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi laudantium quia reprehenderit, harum perferendis, laborum ratione expedita veniam nihil numquam molestias distinctio at quae? Quisquam omnis quo iusto esse non!" 
link="github.com" 
linktext=""/>
</div>

</template>

<style scoped lang="scss">
.container {
    width: 80vw;
    height: 80vh;
    position: fixed;
    background-color: rgba($black, 0.9);
    border: solid $white 1px;
    backdrop-filter: blur(20px);
    top: 10vh;
    left: 10vw;
    z-index: 10;

    h1 {
        text-align: center;
        margin-top: 30px;
        margin-bottom: 20px;
    }
}
</style>