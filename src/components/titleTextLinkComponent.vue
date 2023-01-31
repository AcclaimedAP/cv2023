<script>

export default {
    props: {
        title: String,
        text: String,
        link: String,
        linktext: String
    }
    
}
</script>

<template>
<div>
    <h2>{{ title }}</h2>
    <p>{{ text }}</p>
    <a v-if="linktext && link" href="{{ link }}">{{ linktext }}</a>
    <a v-else-if="link && !linktext" href="{{ link }}">{{ link }}</a>
</div>
</template>

<style scoped lang="scss">
div {
width: 100%;
margin: 30px;
h2 {
    margin: 16px;
}
a {
    text-decoration: none;
    color: $yellow;
    &:hover {
        text-shadow: 0px 0px 2px rgba($white, 0.5);
    }
}
}
</style>