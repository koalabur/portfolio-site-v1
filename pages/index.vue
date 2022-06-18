<template>
  <div>
    <Nav />
    <Intro />
    <About />
  </div>
</template>

<script>
import Nav from '@/components/Nav/v1.vue';
import Intro from '@/components/Intro/v1.vue';
import About from '@/components/About/v1.vue';
export default {
  components: {
    Nav,
    Intro,
    About
  },
  name: 'IndexPage'
}
</script>