<template>
  <div id="app">
    <Header />
    <router-view />
    <Footer />
  </div>
</template>

<script>
import Header from './components/MyHeader.vue'
import Footer from './components/MyFooter.vue'

export default {
  name: "App",
  components: {
    Header,
    Footer
  }
}
</script>

<style>

</style>
