<template>
  <div id="app">
    <SiteHeader :menu="menuHeader"/>
    <SiteMain/>
    <SiteFooter/>
  </div>
</template>

<script>
import SiteHeader from './components/SiteHeader.vue'
import SiteMain from './components/SiteMain.vue'
import SiteFooter from './components/SiteFooter.vue'

export default {
  name: 'App',
  components: {
    SiteHeader,
    SiteMain,
    SiteFooter
  },
  data() {
    return {
      menuHeader: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"]
    }
  }
}
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap.scss";

body {
  font-family: Arial, Helvetica, sans-serif;
}
</style>