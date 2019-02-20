<template>
  <div>
    <Header />
    <div class="min-container-height">
      <nuxt />
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from './Header.vue'
import Footer from './Footer.vue'

export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style>
body {
  color: grey;
}

.min-container-height {
  min-height: calc(80vh - 52px);
}
</style>
