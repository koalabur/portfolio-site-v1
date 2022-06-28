<template>
<div>
    <SiteNavV1 :navList="navListData" />
    <h1>hi</h1>
    <AboutV1 />
</div>
</template>

<script>
export default {
    data() {
        return {
            navListData: [
                {
                    id: "about",
                    title: "About",
                    isActive: false,
                },
                {
                    id: "portfolio",
                    title: "Portfolio",
                    isActive: false,
                }
            ],
        };
    }
}
</script>