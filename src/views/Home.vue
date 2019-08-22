<template>
  <div class="home ">



 <main id="page-wrap">

        <img src="../assets/checklist2a.jpg">
        <PageHeader message="My ToDo List"/>



        <MainBody class="main"/>

 </main>
  </div>
</template>


<script>

import PageHeader from '@/components/PageHeader.vue'
import MainBody from  '@/components/MainBody.vue'
import   Slide   from '../App.vue'


export default {
  name: 'home',
  components: {
    PageHeader,
    MainBody,
    Slide,

  }
}
</script>

<style scoped>




</style>
