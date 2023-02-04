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
    <summary>
        <img v-if="icon" v-bind="imageAttributes" />
        {{ name }}
    </summary>
    <p>{{ info }}</p>
</details>
</template>

<style scoped lang="scss">
img {
    height: 30px;
    width: 30px;
    transform: translate(-16px, 6px);

    position: relative;
    display: inline-block;
}

details {
    margin-bottom: 6px;
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
        font-weight: 700;
        letter-spacing: 2.5px;
        transition: all 0.2s;
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
    }
}
details[open] > summary::after {
  transform: rotate(-135deg);
}
</style>