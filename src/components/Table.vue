<template>
  <div>
    <b-table
      hover
      striped
      head-variant="dark"
      :items="users"
      :fields="fields"
      :filter="filtered"
    ></b-table>
  </div>
</template>

<script>
export default {
  name: "UsersTable",
  props: ["users", "filtered"],
  data() {
    return {
      fields: [
        { key: "first_name", sortable: true },
        { key: "last_name", sortable: true },
        { key: "city", sortable: true },
        { key: "phone_number" },
        { key: "email", label: "Email Address" },
        { key: "createdAt", sortable: true, label: "User Created" },
      ],
    };
  },
};
</script>

<style>
</style>
