<template>
<div class="app">
  <div class="container list-app">
    <div>
      <WeekDay v-for="(item, id) in listItems"
                v-bind:key='id'
                v-bind:weekday="item"
                @delete-listitem= buttonClicked />
    </div>
  </div>
</div>
</template>

<script>
import WeekDay from './components/WeekDay';
export default {
  name: 'App',
  components: { WeekDay },
  data() {
    return {
      listItems: [
        {id: 1, day: "Sunday"},
        {id: 2, day: "Monday"},
        {id: 3, day: "Tuesday"},
        {id: 4, day: "Wednesday"},
        {id: 5, day: "Thursday"},
        {id: 6, day: "Friday"},
        {id: 7, day: "Saturday"}
      ]
    }
  },
  methods: {
    buttonClicked(e) {
        console.log("delete button clicked for row " + e.id);

        //Splice returns removed items and modifies the original array. Hence not a good approach
        // this.listItems.splice(e.id-1, 1, e.id+1);

        //Approach 1:
        // let newList = [];
        // for( let obj of this.listItems) {
        //   if(obj.id === e.id) continue;
        //   newList.push(obj);
        // }
        // this.listItems = newList;

        //Approach 2:
        this.listItems = this.listItems.filter( obj => obj.id != e.id);

        console.log(e);
        console.log(this.listItems);
      }
  },
}
</script>

<style>
.app {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: cursive;
}
.list-app {
  margin-top: 10px;
}

</style>

