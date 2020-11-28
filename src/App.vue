<template>
  <div id="app"></div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      users: [],
    };
  },

  methods: {},
  async created() {
    await fetch("https://5fbc04c1c09c200016d4160c.mockapi.io/api/v1/customers")
      .then((res) => res.json())
      .then((users) => {
        this.users = users;
      })
      .catch((err) => console.log(err));
  },
};
</script>

<style lang="scss">
</style>
