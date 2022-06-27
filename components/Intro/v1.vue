<template>
    <section class="intro">
        <img class="intro__img" src="img/koala-hero.png" width="423" height="385" />
        <h1 class="intro__title">i'm just a web guy doing web guy things</h1>
        <img @click="scrollDown" class="intro__img intro__img--mouse" src="img/mouse-solid.svg" />
    </section>
</template>

<script>
    export default {
        methods: {
            scrollDown() {
                document.querySelector('[data-about]').scrollIntoView({behavior: "smooth"});
            }
        } 
    }
</script>

<style lang="scss" scoped>
    .intro {
        @include section-spacing;
        display: flex;
        flex-direction: column;
        align-items: center;
        padding-top: 7rem;
        background: rgb(42,39,115);
        background: -moz-linear-gradient(180deg, rgba(42,39,115,1) 0%, rgba(28,18,64,1) 100%);
        background: -webkit-linear-gradient(180deg, rgba(42,39,115,1) 0%, rgba(28,18,64,1) 100%);
        background: linear-gradient(180deg, rgba(42,39,115,1) 0%, rgba(28,18,64,1) 100%);
        filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#2a2773",endColorstr="#1c1240",GradientType=1);

        &__img {
            margin-bottom: 1rem;
            @include edge-padding;

            &--mouse {
                filter: invert(87%) sepia(4%) saturate(1432%) hue-rotate(196deg) brightness(99%) contrast(91%);
                animation: bounceAnimation 2s ease 0s infinite alternate forwards;
                width: 75px;
                height: auto;
                cursor: pointer;

                @include bounce-animation;
            }
        }

        &__title {
            font-family: $base-font;
            color: $base-color;
            text-transform: lowercase;
            font-size: 3.5rem;
            font-weight: 200;
            margin-bottom: 1rem;
            text-align: center;
            @include edge-padding;

            @include small-screens {
                font-size: 3rem;
                margin-bottom: 2rem;
            }
        }
    }
</style>