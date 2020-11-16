<template>
  <div>
    <ul v-for="(item, id) in listItems" v-bind:key="id">
      <li> {{listItems[id].title}} </li>
    </ul>
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
        {id: 3, title: "Tuesday"},
        {id: 4, title: "Wednesday"},
        {id: 5, title: "Thursday"},
        {id: 6, title: "Friday"},
        {id: 7, title: "Saturday"}
      ]
    }
  },
}
</script>

<style>

</style>