<template>
  <Header></Header>
    <router-view></router-view>
  <Footer></Footer>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'

export default {
 name: "App",
 components: {
   Header,
   Footer
 }
}
</script>


<style lang="scss">
@import "./scss/_variables.scss";
body, html{
  max-width: 100vw;
  margin: 0;
  padding: 0;
  
}

#app {
  font-family: $font-family;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $black;
  height: 100%;
}

</style>
