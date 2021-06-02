<template>
  <div>
    <span>FullName : {{ fullName }}</span>
    <br />
    <span>Age: {{ age }}</span>
    <br />
    <span>Programming Languages: </span>
    <li v-for="item in lang" :key="item">{{ item }}</li>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fullName: this.$route.query.fullname,
      age: this.$route.query.age,
      lang: this.$route.query.lang,
    };
  },
};
</script>

<style>
</style>