<template>
    <section id="about" class="about" data-about>
        <div class="about__title">
            <h1 class="about__title-text">< who am i? /></h1>
            <div class="about__title-divider"></div>
            <div>
                <img
                    class="about__title-icon"
                    src="img/mouse-icon.png"
                    alt="Mouse"
                    width="18"
                    height="18"
                    loading="lazy"
                    decoding="async"
                />
                <img
                    class="about__title-icon about__title-icon--controller"
                    src="img/controller-icon.png"
                    alt="Controller"
                    width="27"
                    height="18"
                    loading="lazy"
                    decoding="async"
                />
            </div>
        </div>
        <h2 class="about__subtitle">
            my name is <strong>cameron</strong>, i am a
            <strong>front end dev</strong> who likes...
        </h2>
        <div class="about__highlights">
            <div class="about__highlights-col">
                <img
                    class="about__highlights-col-img"
                    src="img/games-icon-lg.png"
                    alt="Games"
                    width="108"
                    height="101"
                    loading="lazy"
                    decoding="async"
                />
                <h3 class="about__highlights-col-title">games</h3>
                <p class="about__highlights-col-subtitle">games are cool</p>
            </div>
            <div class="about__highlights-col">
                <img
                    class="about__highlights-col-img"
                    src="img/anime-icon-lg.png"
                    alt="Anime"
                    width="78"
                    height="101"
                    loading="lazy"
                    decoding="async"
                />
                <h3 class="about__highlights-col-title">anime</h3>
                <p class="about__highlights-col-subtitle">anime is cool too</p>
            </div>
            <div class="about__highlights-col">
                <img
                    class="about__highlights-col-img"
                    src="img/memes-lg.png"
                    alt="Memes"
                    width="134"
                    height="101"
                    loading="lazy"
                    decoding="async"
                />
                <h3 class="about__highlights-col-title">memes</h3>
                <p class="about__highlights-col-subtitle">
                    memes are really cool
                </p>
            </div>
            <div class="about__highlights-col about__highlights-col--special">
                <img
                    class="
                        about__highlights-col-img
                        about__highlights-col-img--rotate
                    "
                    src="img/rgb-lg.png"
                    alt="RGB"
                    width="101"
                    height="101"
                    loading="lazy"
                    decoding="async"
                />
                <h3 class="about__highlights-col-title">rgb</h3>
                <p class="about__highlights-col-subtitle">rgb is super cool</p>
            </div>
        </div>
        <div class="about__divider"></div>
        <div class="about__title">
            <h1 class="about__title-text">
                < i know cool codey (and non codey) things like />
            </h1>
            <div class="about__title-divider"></div>
            <div>
                <img
                    class="about__title-icon"
                    src="img/bug-icon.png"
                    alt="Bug"
                    width="20"
                    height="18"
                    loading="lazy"
                    decoding="async"
                />
                <img
                    class="about__title-icon about__title-icon--controller"
                    src="img/web-icon.png"
                    alt="Web"
                    width="34"
                    height="18"
                    loading="lazy"
                    decoding="async"
                />
            </div>
        </div>
        <div class="about__resume">
            <div class="about__resume-row">
                <p
                    class="
                        about__resume-row-content about__resume-row-content--tl
                    "
                >
                    html
                </p>
                <p class="about__resume-row-content">css</p>
                <p class="about__resume-row-content">javascript</p>
                <p class="about__resume-row-content">vue2</p>
                <p
                    class="
                        about__resume-row-content about__resume-row-content--tr
                    "
                >
                    wordpress
                </p>
            </div>
            <div class="about__resume-row">
                <p
                    class="
                        about__resume-row-content about__resume-row-content--bl
                    "
                >
                    page performance optimization
                </p>
                <p class="about__resume-row-content">adobe creative cloud</p>
                <p class="about__resume-row-content">branding</p>
                <p class="about__resume-row-content">
                    wire-framing/ prototyping
                </p>
                <p
                    class="
                        about__resume-row-content about__resume-row-content--br
                    "
                >
                    video editing
                </p>
            </div>
        </div>
    </section>
</template>

<script>
export default {

};
</script>

<style lang="scss" scoped>
.about {
    @include section-width;
    @include edge-padding;
    @include section-spacing;

    &__divider {
        background-image: linear-gradient(#af27f2, #4003fe);
        width: 2px;
        height: 350px;
        margin: 2rem 0;

        @include small-screens {
            margin-left: auto;
            margin-right: auto;
        }
    }

    &__highlights {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;

        @include small-screens {
            flex-direction: column;
        }

        &-col {
            background-color: rgba(64, 52, 109, 0.6);
            height: auto;
            text-align: center;
            width: 25%;
            padding: 3rem 0.75rem;

            @include small-screens {
                width: 100%;
            }

            &-img {
                margin-bottom: 0.5rem;

                &--rotate {
                    @include rotate-animation;
                    animation: rotate-animation 1500ms linear 0s infinite normal
                        none;
                }
            }

            &--special {
                background-image: linear-gradient(
                    130deg,
                    rgba(175, 39, 242, 0.6),
                    rgba(64, 3, 254, 0.6)
                );
            }

            &-subtitle {
                font-family: $base-font;
                color: $base-color;
                font-size: 1.1rem;
                font-weight: 400;
            }

            &-title {
                font-family: $base-font;
                color: $base-color;
                font-size: 2.2rem;
                font-weight: 200;
                margin-bottom: 0.5rem;
            }
        }
    }

    &__resume {
        display: flex;
        flex-direction: column;
        flex-wrap: nowrap;

        &-row {
            display: flex;
            flex-direction: row;
            flex-wrap: nowrap;

            @include small-screens {
                flex-direction: column;
            }

            &-content {
                font-family: $base-font;
                color: $base-color;
                font-size: 1.1rem;
                text-align: center;
                line-height: 120%;
                margin: auto;
                padding: 0rem 1rem;
                background: rgba(64, 52, 109, 0.6);
                transition: 0.25s ease-in-out;
                max-width: 20%;
                width: 100%;
                height: 135px;
                display: flex;
                align-items: center;
                justify-content: center;
                position: relative;

                @include small-screens {
                    max-width: 100%;
                }

                &--bl {
                    border-bottom-left-radius: 10px;

                    @include small-screens {
                        border-radius: 0;
                    }

                    &:before {
                        border-bottom-left-radius: 10px;

                        @include small-screens {
                            border-radius: 0;
                        }
                    }
                }

                &--br {
                    border-bottom-right-radius: 10px;

                    @include small-screens {
                        border-bottom-left-radius: 10px;
                        border-bottom-right-radius: 10px;
                    }

                    &:before {
                        border-bottom-right-radius: 10px;

                        @include small-screens {
                            border-bottom-left-radius: 10px;
                            border-bottom-right-radius: 10px;
                        }
                    }
                }

                &:hover {
                    background: transparent;
                }

                &:before {
                    position: absolute;
                    content: "";
                    top: 0;
                    right: 0;
                    bottom: 0;
                    left: 0;
                    background-image: linear-gradient(
                        to right,
                        hsla(255, 99%, 50%, 1),
                        hsla(282, 89%, 55%, 1)
                    );
                    z-index: -1;
                    transition: opacity 0.25s linear;
                    opacity: 0;
                }

                &:hover::before {
                    opacity: 1;
                }

                &--tl {
                    border-top-left-radius: 10px;

                    @include small-screens {
                        border-top-left-radius: 10px;
                        border-top-right-radius: 10px;
                    }

                    &:before {
                        border-top-left-radius: 10px;

                        @include small-screens {
                            border-top-left-radius: 10px;
                            border-top-right-radius: 10px;
                        }
                    }
                }

                &--tr {
                    border-top-right-radius: 10px;

                    @include small-screens {
                        border-radius: 0;
                    }

                    &:before {
                        border-top-right-radius: 10px;

                        @include small-screens {
                            border-radius: 0;
                        }
                    }
                }
            }
        }
    }

    &__subtitle {
        font-family: $base-font;
        color: $base-color;
        font-size: 1.3rem;
        font-weight: 400;
        margin-bottom: 3rem;
    }

    &__title {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: center;
        margin-bottom: 2.5rem;

        &-divider {
            height: 1px;
            width: 200px;
            background: #af27f2;
            margin: 5px 15px 0px 10px;

            @include small-screens {
                display: none;
            }
        }

        &-icon {
            margin-top: 5px;
            margin-left: 2px;
            margin-right: 2px;

            &--controller {
                margin-top: 0;
            }

            @include small-screens {
                display: none;
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