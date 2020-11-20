<template>
  <div class="week-day">
      {{weekday.day}}
  </div>
</template>

<script>
export default {
    name: 'WeekDay',
    props: ['weekday'],

}
</script>

<style>
.week-day {
  padding: 8px;
  background: rgb(212, 211, 211);
  border-style: solid;
  border-color: white;
}


</style>