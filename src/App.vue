<template>
  <Home></Home>
</template>

<script>
import Home from '@/views/Home.vue'
export default {
 name: "App",
 components: {
   Home
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
