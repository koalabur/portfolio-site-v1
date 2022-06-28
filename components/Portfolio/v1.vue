<template>
    <section id="portfolio" class="portfolio" data-portfolio>
        <h1 class="portfolio__title">{{ title }}</h1>
        <div class="portfolio__row">
            <div v-for="item in portfolios" :key="item.id">
                <a class="portfolio__row-link" :href="item.link" target="_blank" rel="external">
                    <img :src="item.img" loading="lazy" decoding="async" />
                </a>

            </div>
        </div>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                title: '< portfolio />',
                portfolios: [
                    {
                        id: 1,
                        img: "img/qllv-desktop.jpg",
                        link: "https://qualityliquidatorslv.com/"
                    },
                    {
                        id: 2,
                        img: "img/rc-desktop.jpg",
                        link: "https://radicallycurly.com/"
                    },
                    {
                        id: 3,
                        img: "img/dxp-desktop.jpg",
                        link: "https://www.dancexpresslv.com/"
                    },
                    {
                        id: 4,
                        img: "img/ddm-desktop.jpg",
                        link: "https://dianadmarie.net/"
                    }
                ]
            }
        },
    }
</script>

<style lang="scss" scoped>
    .portfolio {
        @include section-width;
        @include edge-padding;
        @include section-spacing;
        margin-bottom: 10rem;

        &__row {
            display: flex;
            flex-direction: row;
            gap: 1.5rem;

            @include small-screens {
                flex-direction: column;
            }

            &-link {
                outline: 5px solid transparent;
                transition: .25s ease-in-out;
                height: 100%;

                img {
                    vertical-align: bottom;
                }

                &:hover, &:focus {
                    outline-color: #b629f2;
                }
            }
        }

        &__title {
            font-family: $base-font;
            font-size: 2.2rem;
            font-weight: 600;
            background: -webkit-linear-gradient(left, #3700ff 0%, #b629f2 45%);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 2.5rem;
        }
    }
</style>