<template>
  <div>
    <ul v-for="(item, id) in list" v-bind:key="id">
      <li> {{item.title}} </li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'WeekDay',
    props: ['list'],

}
</script>

<style>

</style>