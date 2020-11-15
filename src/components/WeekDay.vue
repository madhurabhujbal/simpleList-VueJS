<template>
  <div>
    <ol v-for="(item, id) in listItems" v-bind:key="id">
      <h3> {{listItems[id].title}} </h3>
    </ol>
  </div>
</template>

<script>
export default {
    name: 'WeekDay',
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