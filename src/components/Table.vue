<template>
  <div class="mt-2">
    <b-table
      show-empty
      hover
      striped
      head-variant="dark"
      :items="users"
      :fields="fields"
      :filter="filtered"
    >
      <template #cell(details)="row">
        <b-button size="small" @click="launchModal(row.item)"
          >Get Full Details</b-button
        >
      </template>
    </b-table>
    <UserModal :userDetails="this.userModal.content" />
  </div>
</template>

<script>
import UserModal from "./Modal.vue";

export default {
  name: "UsersTable",
  components: { UserModal },
  props: ["users", "filtered"],
  data() {
    return {
      fields: [
        { key: "first_name", sortable: true },
        { key: "last_name", sortable: true },
        { key: "city", sortable: true },
        { key: "email", label: "Email Address" },
        { key: "Details", label: "User Details" },
      ],
      userModal: {
        id: "userModal",
        content: "",
      },
    };
  },
  methods: {
    launchModal(user) {
      this.userModal.content = user;
      this.$bvModal.show(this.userModal.id);
    },
  },
};
</script>

<style>
</style>
