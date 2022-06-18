<template>
    <nav class="site-nav">
        <a class="site-nav__link" href="#">about</a>
        <a class="site-nav__link" href="#">portfolio</a>
    </nav>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
    .site-nav {
        position: fixed;
        display: flex;
        flex-direction: row;
        justify-content: center;
        gap: 1.5rem;
        width: 100%;
        margin-top: 1rem;

        &__link {
            font-family: $base-font;
            font-weight: 400;
            font-size: 1.1rem;
            border-radius: 7px;
            transition: .25s ease-in-out;
            z-index: 1;
            background: rgba(64,52,109,.4);
            color: $base-color;
            text-decoration: none;
            padding: .7rem 1rem;
        }
    }
</style>