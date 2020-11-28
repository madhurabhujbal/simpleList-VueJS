<template>
  <div class="row">
    <div :class="'col-md-2 ' + getId()">
      {{weekday.day}}
    </div>
    <div class="col-md-2">
      <button @click="buttonClicked">Delete</button>
    </div>
  </div>
</template>

<script>
export default {
    name: 'WeekDay',
    props: ['weekday'],
    methods: {
      getId() {
        return this.weekday.id % 2 === 0 ? "even-day" : "odd-day";
      },
    }
}
</script>

<style>

.even-day {
  padding: 8px;
  background: rgb(212, 211, 211);
  border-style: solid;
  border-color: white;
  text-align: center;
}

.odd-day {
  padding: 8px;
  background: rgb(238, 207, 207);
  border-style: solid;
  border-color: white;
  text-align: center;
}

button {
  padding: 8px;
  background: rgb(128, 161, 206);
  margin-left: 30px;
  border-style: solid;
  border-color: white;
}

</style>
