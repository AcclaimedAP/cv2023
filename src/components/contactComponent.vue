<script>

export default {
    props: {
        link: String,
        linktext: String,
        image: String,
        imageAltText: { type: String, default: "Project image"},
        imgW: { type: Number, default: 200},
        imgH: { type: Number, default: 170 },
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
    <h2><a v-if="linktext && link" v-bind:href="link">{{ linktext }}</a>
    <a v-else-if="link && !linktext" v-bind:href="link">{{ link }}</a></h2>

</div>
</template>

<style scoped lang="scss">
img{
    width: 150px;
    height: auto;
}
div {
margin: 30px;
width: 150px;

h2 {
    margin: 16px;
    line-height: 2.5rem;
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