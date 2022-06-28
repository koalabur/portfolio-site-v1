<template>
    <div ref="site">
        <SiteNavV1 :navList="navList" />
        <IntroV1 ref="sectionIntro" />
        <AboutV1 ref="sectionAbout" />
        <PortfolioV1 ref="sectionPortfolio" />
        <SiteFooterV1 />
    </div>
</template>

<script>
export default {
    data() {
        return {
            observer: null,
            observerOptions: {
                root: this.$el,
                rootMargin: "0px",
            },
            navList: [
                {
                    id: "about",
                    title: "About",
                    isActive: false,
                },
                {
                    id: "portfolio",
                    title: "Portfolio",
                    isActive: false,
                },
            ],
        };
    },
    beforeMount() {
        this.observer = new IntersectionObserver(this.onElementObserved, this.observerOptions);
    },
    mounted() {
        this.observeSections(['sectionPortfolio', 'sectionAbout', 'sectionIntro'])
    },
    beforeDestroy() {
        this.observer.disconnect();
    },
    methods: {
        onElementObserved(entries) {
            entries.forEach(({ intersectionRatio, target }) => {
                if (intersectionRatio > 0) {
                    this.navList.forEach((listItem, i, list) => {
                        const isActive = listItem.id === target.id ? true : false
                        this.navList[i].isActive = isActive
                    })
                }
            });
        },
        observeSections(sectionList) {
            sectionList.forEach((section) => this.observer.observe(this.$refs[section].$el))
        }
    },
};
</script>