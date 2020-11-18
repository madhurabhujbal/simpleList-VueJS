<template>
  <div>
    <ol>
      <li v-for="(item, id) in list" v-bind:key='id'> {{item.title}} </li>
    </ol>
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