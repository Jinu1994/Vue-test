<template>
  <div>
    <h5>Question 6</h5>
    <div class="container-1">
      Render all items whose Ids are multiple of 2 here
      <div v-for ="student in students" :key="student.id">
        <ul v-if="student.id % 2 === 0">
          <li>{{student.name}}</li>
        </ul>
      </div>
  </div>
    <div class="container-2">
      Render all items whose Ids are multiples of 3 here
      <div v-for ="student in students" :key="student.id">
        <ul v-if="student.id % 3 === 0">
          <li>{{student.name}}</li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      students: [
        {
          id: 4,
          name: "Eve",
        },
        {
          id: 2,
          name: "Holt",
        },
        {
          id: 3,
          name: "Morris",
        },
        {
          id: 6,
          name: "Charles",
        },
        {
          id: 9,
          name: "Tracey",
        },
        {
          id: 15,
          name: "Ramos",
        },
        {
          id: 1,
          name: "Sam",
        },
      ],
    };
  },
};
</script>
<style>
.container-1 {
  min-height: 50px;
  background: beige;
  margin: 20px;
}
.container-2 {
  min-height: 50px;
  background: lightblue;
  margin: 20px;
}
</style>

