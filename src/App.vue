<template>
  <div id="app">
    <b-container fluid>
      <UsersTable :users="users" />
    </b-container>
  </div>
</template>

<script>
import UsersTable from "./components/Table.vue";

export default {
  name: "App",
  components: { UsersTable },
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
