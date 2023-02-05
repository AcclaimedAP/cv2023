<script>
import contact from './contactComponent.vue';

export default {
    components: {
        contact,
    }
}
</script>

<template>
<div class="container">
<h1>Kontakta mig</h1>
    <div class="contacts">
        <contact link="https://github.com/AcclaimedAP" 
        linktext="Github"
        image="./img/contact/github-mark-white.svg" 
        imageAltText="Github Logo"/>
        <contact link="mailto:alexander.pressfelt@medieinstitutet.se" 
        linktext="E-Mail"
        image="./img/contact/mail-white.svg" 
        imageAltText="Mail icon"/>
        <contact text="Acclaimed#5648"
        image="./img/contact/discord-mark-white.svg" 
        imageAltText="Discord logo"/>
        <contact link="https://www.linkedin.com/in/alexander-pressfelt-559754145/" 
        linktext="LinkedIn"
        image="./img/contact/linkedin-svgrepo-com.svg" 
        imageAltText="LinkedIn Logo"/>
    </div>
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
    .contacts {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
    }
    h1 {
        text-align: center;
        margin-top: 30px;
        margin-bottom: 20px;
    }
}
</style>