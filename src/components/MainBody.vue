<template>
<div>

        <article class="message is-dark">
                <div class="message-header">
                        <input
                        class="input"
                        type="text"
                        placeholder=""
                        v-model="newItem"
                        @keyup.enter="saveItem">

                        <button class="button "
                        style="margin-left: 20px; background-color: #f07109"
                        :disabled="newItem.length === 0"
                        @click="saveItem"
                              ><span class="icon">
                                <i class="fas fa-plus"></i>
                              </span></button>

                </div>

                            <ul>
                                <li v-bind:key="item.id" v-for="item in items">
                                    <p class="panel-block " style="display: block" >
                                        {{item}}
                                        <button
                                        class="delete"
                                        aria-label="delete"
                                        @click="removeElement(item)"
                                        style="float: right !important"
                                        ></button>
                                    </p>
                                </li>
                            </ul>

        </article>


</div>

</template>


<script>


export default {

    data() {
      return {
        newItem: '',
        items: []

      }
    },
        methods: {
        saveItem: function () {
            if (this.newItem.length != 0) {
            this.items.push(this.newItem)
            this.newItem = ''
            }
        },

        removeElement (item) {
            var itemIndex =  this.items.indexOf(item)
            this.items.splice(itemIndex, 1)
        },

    }
  }

</script>

<style>
article{
  margin-top: -60px;
}
@media only screen and (max-width: 600px) {
article{
  margin-top: 0
}
}
</style>
