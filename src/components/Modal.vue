<template>
  <b-modal id="userModal">
    <ul v-for="item in userDetails" :key="item.id">
      <li>
        <!-- Filter through userDetails object and match keys with the value so I could add them to list as well -->
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
};
</script>
