<template>
  <b-modal id="userModal">
    <ul v-for="item in userDetails" :key="item.id">
      <li>
        {{
          Object.keys(userDetails).find(function (key) {
            return userDetails[key] === item;
          })
        }}: {{ item }}
      </li>
    </ul>
  </b-modal>
</template>

<script>
export default {
  name: "UserModal",
  props: ["userDetails"],
  methods: {
    log(m) {
      return console.log(m);
    },
  },
};
</script>

<style>
</style>
