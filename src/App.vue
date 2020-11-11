<template>
<div>
  <li v-for="(item, id) in listItems" v-bind:key="id">
    {{item.title}}
  </li>
  <button @click="buttonClicked">Button</button>
</div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      listItems: [
        {id: 1, title: "Sunday"},
        {id: 2, title: "Monday"},
        {id: 3, title: "Tuesday"}
      ]
    }
  },
  methods: {
    buttonClicked() {
      this.title = "button clicked"
}
  }

}
</script>

<style>

</style>
