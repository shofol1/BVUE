<script>
import HookVue from "./components/Hook.vue";
import axios from "axios";

export default {
  name: "App",
  data() {
    return {
      users: [],
    };
  },
  created() {
    axios
      .get("https://jsonplaceholder.typicode.com/users")
      .then((res) => (this.users = res.data))
      .catch((err) => console.log(err));
  },
  components: {
    HookVue,
  },
  methods: {},
};
</script>

<template>
  <HookVue></HookVue>
  <ul v-for="(user, i) in users" :key="user.id">
    <li>{{ user.name }}</li>
  </ul>
</template>
