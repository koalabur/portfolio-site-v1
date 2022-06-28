<template>
    <footer class="footer">
        <a href="https://www.linkedin.com/in/cameron-roberts-design/" target="_blank" rel="external">
            <img class="footer__img" src="img/linkedin-icon.svg" width="75" height="75" alt="linked in">
        </a>
        <p class="footer__copyright">© {{currentDate.getFullYear()}} Cameron Roberts.</p>
    </footer>
</template>

<script>
    export default {
        data() {
            return {
                currentDate: new Date,
            }
        }
    }
</script>

<style lang="scss" scoped>
    .footer {
        @include edge-padding;
        @include section-width;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding-bottom: 2rem;

        &__copyright {
            font-family: $base-font;
            color: $base-color;
            font-size: 1rem;
        }

        &__img {
            margin-bottom: 1rem;
        }
    }
</style>