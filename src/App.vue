<template>
<div>
  <DaysOfWeek />
  <button @click="buttonClicked">Button</button>
</div>
</template>

<script>
import DaysOfWeek from './components/DaysOfWeek';
export default {
  name: 'App',
  componenets: { DaysOfWeek },
  methods: {
    buttonClicked() {
      this.title = "button clicked"
}
  }

}
</script>

<style>

</style>
