<template>
<div id="mainAbout">

  <Slide/>

  <div class="credentials">
    <Credentials credentialsInfo="Created by"/><br>
  </div>

<div id="line"></div>
  <div id="gridtech">Used technologies:
<div class="columns is-mobile">
 <div class="column is-half-mobile"><i class="fab fa-vuejs fa-7x"></i></div>
 <div class="column is-half-mobile"><img :src="image2" alt="bulma" /></div>

</div>
<div class="columns is-mobile">
  <div class="column is-half-mobile"><img v-bind:src="image1" alt="PWA" /></div>
  <div class="column is-half-mobile"><i class="fab fa-sass fa-7x"></i></div>
</div>
<div class="columns is-mobile">
  <div class="column is-half-mobile"><i class="fab fa-npm fa-7x"></i></div>
  <div class="column is-half-mobile"><i class="fab fa-js fa-7x"></i></div>
</div>
  </div>
</div>
</template>

<script>

import Credentials from '@/components/Credentials.vue'
import Slide from '../App.vue'

export default {
  name: 'about',
  components: {
    Credentials,
    Slide
  },
  data () {
    return {
      image1: require('../assets/bulma.png'),
      image2: require('../assets/pwa.png')
    }
  }
}
</script>

<style scoped>
#mainAbout {
 margin-top: 15px;

}
#gridtech{
margin: 5% 20px
}
#line{
  width:100%;
  background-color: red;
  height: 2px;
}
img {
 width: 30%
}
.columns{
  margin-top: 5%
}

.column{
  max-width: 50% !important;
}
@media only screen and (max-width: 600px) {

img {
 width: 50%;
}

}
</style>
