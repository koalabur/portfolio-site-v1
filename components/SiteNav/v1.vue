<template>
    <div>
        <a class="notice" href="https://www.cameronrdesign.com/"
            >You're currently viewing the vue2/ nuxtjs portfolio. Click this bar
            to visit the wordpress portfolio.</a
        >

        <nav class="site-nav">
            <a
                v-for="item in navList"
                :ref="item.id"
                class="site-nav__link"
                :class="{ '-isActive': item.isActive }"
                @click="scrollTo(item.id, $event)"
                >
                {{ item.title }}
            </a>
        </nav>
    </div>
</template>

<script>
export default {
    props: {
        navList: Array,
    },
    methods: {
        scrollTo(elId, e) {
            console.log(e)
            e.preventDefault();
            document
                .getElementById(elId)
                .scrollIntoView({ behavior: "smooth" });
        },
    },

    mounted() {
        console.log('sitenav mounted')
    },
};
</script>

<style lang="scss" scoped>
.notice {
    @include edge-padding;
    font-family: $base-font;
    background: #42b883;
    color: #fff;
    font-size: calc(0.8rem + 0.2vw);
    text-align: center;
    position: fixed;
    width: 100%;
    padding: 0.4rem 0;
    z-index: 1;
    text-decoration: none;
}
.site-nav {
    position: fixed;
    display: flex;
    flex-direction: row;
    justify-content: center;
    gap: 1.5rem;
    width: 100%;
    margin-top: 3rem;
    z-index: 1;

    @include small-screens {
        margin-top: 4rem;
    }

    &__link {
        font-family: $base-font;
        font-weight: 400;
        font-size: 1.1rem;
        border-radius: 7px;
        transition: 0.25s ease-in-out;
        z-index: 1;
        background: rgba(64, 52, 109, 0.4);
        color: $base-color;
        text-decoration: none;
        padding: 0.7rem 1rem;
        cursor: pointer;
        border: none;
        transition: 0.25s ease-in-out;

        &.-isActive {
            background: rgb(175, 39, 242);
            background: -moz-linear-gradient(
                90deg,
                rgba(175, 39, 242, 1) 0%,
                rgba(64, 3, 254, 1) 100%
            );
            background: -webkit-linear-gradient(
                90deg,
                rgba(175, 39, 242, 1) 0%,
                rgba(64, 3, 254, 1) 100%
            );
            background: linear-gradient(
                90deg,
                rgba(175, 39, 242, 1) 0%,
                rgba(64, 3, 254, 1) 100%
            );
            filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#af27f2",endColorstr="#4003fe",GradientType=1);
            transition: 0.25s ease-in-out;
        }

        // &--active:before {
        //     position: absolute;
        //     content: "";
        //     top: 0;
        //     right: 0;
        //     bottom: 0;
        //     left: 0;
        //     background-image: linear-gradient( to right, hsla(255, 99%, 50%, 1), hsla(282, 89%, 55%, 1) );
        //     z-index: -1;
        //     transition: opacity .25s linear;
        //     opacity: 1;
        //     border-radius: 6px;
        //     width: auto;
        // }
    }
}
</style>