<template>
  <div class="home">

 <main id="page-wrap">
  <img src="../assets/checklist1.jpg">
  <PageHeader message="My ToDo List"/>
  <MainBody class="main"/>
 </main>

<div class="modal is-active is-clipped">
  <div class="modal-background"></div>
  <div class="modal-content">
    <p>Please note:</p>
    <p>This website is a Progressive Web App dedicated mostly for mobile devices.</p>
    <p>It still can be used on any desktop device, while keeping 100% if its functionality.</p>
    <p>Enjoy!.</p>
  </div>
  <button @click="closeIt" class="modal-close is-large" aria-label="close"></button>
</div>

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
  },
  methods: {
    closeIt: function() {
      document.querySelector('.modal').classList.remove('is-active')
    }
  }
}
</script>

<style scoped>
@media screen and (max-width: 1025px) {
  .modal {
    display: none;
  }
}
.modal-content{
  background-color: aliceblue;
  padding: 1%;
  border-radius: 5px
}
</style>
