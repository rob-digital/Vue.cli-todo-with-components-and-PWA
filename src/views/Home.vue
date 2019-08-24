<template>
  <div class="home ">

 <main id="page-wrap">
        <img src="../assets/checklist1.jpg">
        <PageHeader message="My ToDo List"/>

          <MainBody class="main"/>
 </main>
</div>
</template>

<script>

import PageHeader from '@/components/PageHeader.vue'
import MainBody from '@/components/MainBody.vue'

export default {
  name: 'home',
  components: {
    PageHeader,
    MainBody
  }
}
</script>
