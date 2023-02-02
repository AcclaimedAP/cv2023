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
details {
    background-color: rgba($white, 0.05);
    text-align: center;
    height: 36px;
    line-height: 36px;
    transition: all 0.2s;

    &:hover {
        background-color: rgba($white, 0.09);
    }
    
    summary {
        background-color: rgba($white, 0.03);

    }
}
</style>