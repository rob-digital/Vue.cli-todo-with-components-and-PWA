<template>
  <div id="app" class="container is-widescreen">

  <Slide right noOverlay>

        <span class="menu-link"><router-link class="menu-link" to="/">
        <i class="fas fa-home"></i>
         Home</router-link></span>

        <span class="menu-link"><router-link to="/about">
        <i class="fas fa-key"></i>
         About</router-link></span>


    </Slide>
    <router-view/>

  </div>
</template>


<script>
import   Slide   from 'vue-burger-menu'
export default {
  components:
  Slide
}
</script>
<style lang="scss">
$orange-color: #f07109;
$block: block;

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: relative;

}



.nav a {
  font-weight: bold;
  color: $orange-color;
}

.menu-link a.router-link-exact-active {
  color: $orange-color;
}

.menu-link a{
  display: $block !important;
   color: $orange-color;
}

</style>
