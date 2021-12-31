<template>
  <Header></Header>
    <router-view></router-view>
  <Footer></Footer>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import AOS from 'aos'
import 'aos/dist/aos.css'

export default {
 name: "App",
 components: {
   Header,
   Footer
 },
 created(){
   AOS.init()
 }
}
</script>


<style lang="scss">
@import "./scss/_variables.scss";

html {
  max-width: 100%;
  height: 100%;
  overflow-x: hidden;
}

body {
  max-width: 100%;
}

html, body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: $font-family;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $black;
  height: 100%;
}

</style>
