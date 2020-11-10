<template>
<div>
  <h2>{{ title }}</h2>
  <button @click="buttonClicked">Button</button>
</div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      title: "hello madhu"
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
