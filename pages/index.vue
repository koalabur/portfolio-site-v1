<template>
  <div>
    <Nav />
    <Intro />
    <About />
    <Portfolio />
    <Footer />
  </div>
</template>

<script>
import Nav from '@/components/Nav/v1.vue';
import Intro from '@/components/Intro/v1.vue';
import About from '@/components/About/v1.vue';
import Portfolio from '@/components/Portfolio/v1.vue';
import Footer from '@/components/Footer/v1.vue';
export default {
  components: {
    Nav,
    Intro,
    About,
    Portfolio,
    Footer
  },
  name: 'IndexPage'
}
</script>