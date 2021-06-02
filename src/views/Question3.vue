<template></template>

<script>
export default {
  beforeCreate() {
    alert("I am being created");
  },
  created() {
    alert("I am created");
  },
  beforeMount() {
    alert("I am about to be introduced to the DOM");
  },
  mounted() {
    alert("I am in the DOM");
  },
  destroyed() {
    alert("I am destroyed");
  },
};
</script>

<style>
</style>