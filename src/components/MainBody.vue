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
                        style="margin-left: 20px; background-color: #ff7f07"

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
        <a class="button "
        id="clearAllButton"
        v-if="items.length !== 0"
        @click="clearAll"
        >Clear All</a>

</div>

</template>


<script>
const STORAGE_KEY = "todo-storage"
export default {

    data() {
      return {
        newItem: '',
        items: [],
        items2: []

      }
    },
     mounted() {
        this.items = JSON.parse(localStorage.getItem(STORAGE_KEY) || '[]')
    },
methods: {
      saveItem: function () {
            if (this.newItem.length != 0) {
            this.items.push(this.newItem)
            this.newItem = ''
            localStorage.setItem(STORAGE_KEY, JSON.stringify(this.items))
            }
        },

        removeElement (item) {
            var itemIndex =  this.items.indexOf(item)
            this.items.splice(itemIndex, 1)
        },
        clearAll: function() {
          this.items = [],
          localStorage.clear()
       }
    }
  }

</script>

<style lang="scss">
$grey: #b6b1b1;
#clearAllButton{
  background-color: $grey;
  color: white;
  margin: 10% 0 5% 0
}
article{
  margin-top: -60px;
}
.message-header{
  border-radius: 0 0 0 0 !important
}
.panel-block{
  text-align: left !important
}
@media only screen and (max-width: 600px) {
article{
  margin-top: -2%
}
}
</style>
