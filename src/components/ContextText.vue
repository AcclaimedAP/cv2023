<script>
export default {
    props: ['title', 'context']
    ,
};

</script>

<template>
    <div>
        <h1>{{ title }}</h1>
        <p>{{ context }}</p>
    </div>
</template>

<style scoped lang="scss">
div {
    background-color: $purple;
    h1{
        margin: 10px;
    }
}
</style>
