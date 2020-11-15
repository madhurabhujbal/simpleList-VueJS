<template>
<div id="app">
    <li><WeekDay /></li>
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

}
</script>

<style>

</style>
