<template>
<div>
  <div class="intro hero  is-bold">
    <h1 class="title is-4"> {{ credentialsInfo }} </h1>
    <Author/>
  </div>

    </div>
</template>


<script>

import Author from './Author.vue'


export default {
  name: 'Credentials',
  props: {
    credentialsInfo: {
      type: String,
      reqiured: true
    },
  },
  components: {
    Author
  }
}


</script>

<style scoped>
.intro{
  margin-top: 5%
}
@media only screen and (max-width: 600px) {

  .title{
    font-size: 1.5em
  }
}

</style>
