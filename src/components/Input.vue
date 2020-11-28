<template>
  <b-input
    type="text"
    v-model="filter"
    placeholder="Search for a user"
    @keyup="inputFilter"
  />
</template>

<script>
export default {
  name: "FilterInput",
  data() {
    return {
      filter: null,
    };
  },
  methods: {
    inputFilter() {
      const that = this;
      // $nextTick helps with updating data with KeyUp so it does not render before filter data is fully registered
      this.$nextTick(() => that.$emit("getFilterInput", that.filter));
    },
  },
};
</script>

<style>
</style>
