<script>
import AllFriendsVue from "./components/AllFriends.vue";
import NavbarVue from "./components/Navbar.vue";
import OnlineFriendsVue from "./components/OnlineFriends.vue";

export default {
  name: "App",
  data() {
    return {};
  },
  components: {
    AllFriendsVue,
    NavbarVue,
    OnlineFriendsVue,
  },
};
</script>

<template>
  <AllFriendsVue></AllFriendsVue>
  <OnlineFriendsVue></OnlineFriendsVue>
</template>
