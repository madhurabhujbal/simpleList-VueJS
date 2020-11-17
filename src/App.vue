<template>
<div>
  <WeekDay v-bind:listItems="listItems" />
  <button @click="buttonClicked">Button</button>
</div>
</template>

<script>
import WeekDay from './components/WeekDay';
export default {
  name: 'App',
  components: { WeekDay },
  data() {
    return {
      listItems: [
        {id: 1, title: "Sunday"},
        {id: 2, title: "Monday"},
        {id: 3, title: "Tuesday"},
        {id: 4, title: "Wednesday"},
        {id: 5, title: "Thursday"},
        {id: 6, title: "Friday"},
        {id: 7, title: "Saturday"}
      ]
    }
  },
  methods: {
    buttonClicked() {
      this.title = "button clicked"
    }
  },

}
</script>

<style>

</style>
