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

<content title="CV i Vue" 
text="Denna sida är mitt första projekt byggt i Vue.js. Målet med sidan är att visa upp mina kunskaper i praktiken samt att uppvisa en förståelse att lära sig ramverk och andra resurser själv. Vue är inte något av de delar som ingår i den undervisning som jag har gått. Den använder sig flitigt av components för att lätt justera innehållet och för att kunna skala den." 
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