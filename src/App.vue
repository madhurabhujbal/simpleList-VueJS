<template>
<div id="app">
  <WeekDay />
  <button @click="buttonClicked">Button</button>
</div>
</template>

<script>
import WeekDay from './components/WeekDays';
export default {
  name: 'App',
  components: { WeekDay },
  methods: {
    buttonClicked() {
      this.title = "button clicked"
}
  }

}
</script>

<style>
button {
  margin-top: 30%;
}
</style>
