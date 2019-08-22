<template>
<div id="mainAbout">

  <Slide/>

  <div class="credentials">
    <Credentials credentialsInfo="Created by"/><br>
  </div>

<div id="line"></div>
  <div id="gridtech">Used technologies:
<div class="columns is-mobile">
 <div class="column"><i class="fab fa-vuejs fa-7x"></i></div>
  <div class="column"><i class="fab fa-sass fa-7x"></i></div>
</div>
<div class="columns is-mobile">
  <div class="column"><i class="fab fa-npm fa-7x"></i></div>
  <div class="column"><i class="fab fa-js fa-7x"></i></div>
</div>
  </div>

</div>
</template>

<script>

import Credentials from '@/components/Credentials.vue'
import   Slide   from '../App.vue'


export default {
  name: 'about',
  components: {
    Credentials,
    Slide

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

.columns{
  margin-top: 5%
}

</style>
