<template>
  <div class="intro hero  is-bold">
    <h1 class="title is-1"> {{ message }} </h1>
  </div>
</template>


<script>
export default {
  props: {
    message: {
      type: String,
      reqiured: true
    }
  }
}
</script>

<style scoped>
  .title{
   display: flex;
      align-items: center;
      position: relative;
      left: 15px;
      top: -60px;
      text-shadow: 2px 2px white
  }

@media only screen and (max-width: 600px) {
   .title{
    display: flex;
      align-items: center;
      position: absolute;
      left: 15px;
     top: 15px;
      font-size: 1.5em;
      text-shadow: 2px 2px white

  }
}
</style>
