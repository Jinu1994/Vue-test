<template>
  <div>
    <h5>Question 7</h5>
    <div class="form-container">
      <!-- Render the form here -->
      <form>
        <div>
          <label for="fullName">Full Name: </label>
          <input
            type="text"
            id="fullName"
            class="form-control"
            v-model="fullName"
          />
        </div>
        <div>
          <label for="fullName">Age: </label>
          <input type="text" id="age" class="form-control" v-model="age" />
        </div>
        <div>
          <span>Gender:</span>
          <label for="male">
            <input type="radio" id="male" value="Male" v-model="gender" /> Male
          </label>
          <label for="female">
            <input type="radio" id="female" value="Female" v-model="gender" />
            Female
          </label>
        </div>
        <div>
          <input
            type="checkbox"
            id="vueJs"
            value="VueJs"
            v-model="selectedLanguages"
          />
          <label for="vueJs">VueJs</label>
          <input
            type="checkbox"
            id="c#"
            value="C#"
            v-model="selectedLanguages"
          />
          <label for="c#">C#</label>
          <input
            type="checkbox"
            id="angular"
            value="Angular"
            v-model="selectedLanguages"
          />
          <label for="angular">Angular</label>
        </div>
        <button class="btn btn-primary" @click.prevent="submitted">
          Submit!
        </button>
      </form>
    </div>
    <div v-if="isSubmitted">
      <span>FullName : {{ fullName }}</span>
      <br />
      <span>Age: {{ age }}</span>
      <br />
      <span>Gender: {{ gender }}</span>
      <br />
      <span>Programming Languages: </span>
      <li v-for="item in selectedLanguages" :key="item">{{ item }}</li>
    </div>
  </div>
</template>
<script>
import router from "../router";
export default {
  data() {
    return {
      fullName: "",
      age: "",
      gender: "",
      selectedLanguages: [],
      isSubmitted: false,
    };
  },
  methods: {
    submitted() {
      this.isSubmitted = true;
      router.push({
        name: "question7b",
        query: {
          fullname: this.fullName,
          age: this.age,
          lang: this.selectedLanguages,
        },
      });
    },
  },
};
</script>

