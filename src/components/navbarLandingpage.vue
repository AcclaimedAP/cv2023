<script>

</script>

<template>
<nav>
    <ul>
        <li>About Me</li>
        <li>Projects</li>
        <li>Contact</li>
    </ul>
</nav>
</template>

<style scoped lang="scss">
nav {
    z-index: 100;
    position: fixed;
    top: 60%;
    left: 50%;
    font-size: 1.6em;
    width: 80vh;
    transform: translateX(-50%);

    ul{
        list-style: none;
        display: flex;
        justify-content: space-evenly;
        flex-direction: row;
        flex-wrap: nowrap;
        li {
            text-align: center;
            transform: translateX(-50%);
            text-shadow: 0 0 5px rgba($color: #000000, $alpha: 0.5);
            display: inline-block;
            position: relative;
            cursor: pointer;
            &:after {
                content: '';
                position: absolute;
                left: 50%;
                bottom: -2px;
                width: 0px;
                height: 2px;
                background: $white;
                transition: all 0.45s;

            }
            &:hover:after {
                    width: 100%;
                    left: 0;

            }
        }
    }
}
</style>
