<template>
  <div>
    <ul v-for="(item, id) in listItems" v-bind:key="id">
      <li> {{item.title}} </li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'WeekDay',
    props: ['listItems'],

}
</script>

<style>

</style>