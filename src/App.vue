<template>
  <div id="app">
    <Header />
    <b-container fluid>
      <FilterInput @getFilterInput="updateFilter" />
      <UsersTable :users="users" :filtered="filter" />
    </b-container>
  </div>
</template>

<script>
import UsersTable from "./components/Table.vue";
import FilterInput from "./components/Input.vue";
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: { UsersTable, FilterInput, Header },
  data() {
    return {
      users: [],
      filter: null,
    };
  },

  methods: {
    updateFilter(e) {
      console.log(e);
      this.filter = e;
    },
  },
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
