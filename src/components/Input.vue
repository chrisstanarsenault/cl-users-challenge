<template>
  <b-input type="text" v-model="filter" placeholder="Search for a user" />
</template>

<script>
export default {
  name: "FilterInput",
  data() {
    return {
      filter: null,
    };
  },
};
</script>

<style>
</style>
