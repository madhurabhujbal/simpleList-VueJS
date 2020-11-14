<template>
<div id="app">
  <ul v-for="(item, id) in listItems" v-bind:key="id">
    <li><WeekDay /></li>
  </ul>
  <button @click="buttonClicked">Button</button>
</div>
</template>

<script>
import WeekDay from './components/WeekDay';
export default {
  name: 'App',
  components: { WeekDay },
  methods: {
    buttonClicked() {
      this.title = "button clicked"
    }
  },
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
/* button {
  margin-top: 30%;
} */
</style>
