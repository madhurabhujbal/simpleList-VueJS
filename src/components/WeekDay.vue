<template>
  <div class="col-md-2 week-day" v-bind:class="getId()">
    <span :class="getId">
      {{weekday.day}}
    </span>
  </div>
</template>

<script>
export default {
    name: 'WeekDay',
    props: ['weekday'],
    methods: {
      getId() {
        return {
          id : ((this.props[0].id)%2==0) ? 'even-day' : 'odd-day'
        }
      }
    }
}
</script>

<style>

.week-day {
  padding: 8px;
  background: rgb(212, 211, 211);
  border-style: solid;
  border-color: white;
}

.odd-day {
  background: brown;
}

</style>