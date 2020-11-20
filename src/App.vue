<template>
<div class="list-app">
    <WeekDay v-for="(item, id) in listItems" v-bind:key='id' v-bind:weekday="item" />
  <button class="button" @click="buttonClicked">Button</button>
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
        {id: 1, day: "Sunday"},
        {id: 2, day: "Monday"},
        {id: 3, day: "Tuesday"},
        {id: 4, day: "Wednesday"},
        {id: 5, day: "Thursday"},
        {id: 6, day: "Friday"},
        {id: 7, day: "Saturday"}
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
.list-app {
margin-left: 9px;
}

.button {
  margin-top: 8px;
}

</style>
