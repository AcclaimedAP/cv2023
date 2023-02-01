<script>
import contact from './contactComponent.vue';

export default {
    components: {
        content,
    }
}
</script>

<template>
<div class="container">
<h1>Kontakta mig</h1>
<contact link="https://github.com/AcclaimedAP" linktext="Github"/>

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