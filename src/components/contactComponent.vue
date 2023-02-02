<script>

export default {
    props: {
        link: String,
        linktext: String,
        image: String,
        imageAltText: { type: String, default: "Project image"},
        imgW: { type: Number, default: 200},
        imgH: { type: Number, default: 170 },
        text: String
    },
    data() {
        return {
            imageAttributes: {
                src: this.image,
                alt: this.imageAltText,
                height: this.imgH,
                width: this.imgW
            }
        }
    }
}
</script>

<template>
<div class="contactContainer">
    <img v-if="image" v-bind="imageAttributes">
    <h2 v-if="link"><a v-if="linktext && link" v-bind:href="link">{{ linktext }}</a>
    <a v-else v-bind:href="link">{{ link }}</a>
    </h2>
    <h2 v-else>{{ text }}</h2>
</div>
</template>

<style scoped lang="scss">
img{
    width: 150px;
    height: auto;
    position: absolute;
    top: 40px;
    left: 50%;
    transform: translateX(-50%);
    
}
div {
margin: 30px;
width: 150px;
height: 200px;
padding: 50px;
padding-bottom: 10px;
border: 1px solid rgba($white, 0.5);
background-color: rgba($white, 0.02);
position: relative;
transition: all 0.6s;

&:hover {
    background-color: rgba($white, 0.07);
    box-shadow: 0px 0px 10px rgba($white, 0.3);
}

h2 {

    line-height: 2.5rem;
    position: absolute;
    bottom: 0px;
    left: 50%;
    transform: translateX(-50%);
}
a {
    display: block;
    text-align: center;
    width: 100%;
    text-decoration: none;
    color: $yellow;
    &:hover {
        text-shadow: 0px 0px 2px rgba($white, 0.5);
    }
}
}
</style>