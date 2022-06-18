<template>
    <section class="about">
        <div class="about__title">
            <h1 class="about__title-text">< who am i? /></h1>
            <div class="about__title-divider"></div>
            <div>
                <img class="about__title-icon" src="@/assets/img/mouse-icon.png" alt="Mouse" width="18" height="18" loading="lazy" decoding="async">
                <img class="about__title-icon--controller" src="@/assets/img/controller-icon.png" alt="Controller" width="27" height="18" loading="lazy" decoding="async">
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
    .about {
        @include section-width;
        @include edge-padding;
        &__title {
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            align-items: center;
            margin-bottom: 2.5rem;

            &-divider {
                height: 1px;
                width: 200px;
                background: #AF27F2;
                margin: 5px 15px 0px 10px;
            }

            &-icon {
                margin-top: 5px;
                margin-left: 2px;
                margin-right: 2px;
                &--controller {
                    margin-top: 0;
                }
            }

            &-text {
                font-family: $base-font;
                font-size: 2.2rem;
                font-weight: 600;
                background: -webkit-linear-gradient(left, #3700ff 0%, #b629f2 45%);
                background-clip: text;
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;
            }
        }
    }
</style>