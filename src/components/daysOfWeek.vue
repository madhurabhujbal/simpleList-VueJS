<template>
  <div>
      <li v-for="(item, id) in listItems" v-bind:key="id">
    {{item.title}}
  </li>
  </div>
</template>

<script>
export default {
    data() {
    return {
      listItems: [
        {id: 1, title: "Sunday"},
        {id: 2, title: "Monday"},
        {id: 3, title: "Tuesday"}
      ]
    }
  },

}
</script>

<style>

</style>