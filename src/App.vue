<script>
import AllFriendsVue from "./components/AllFriends.vue";
import NavbarVue from "./components/Navbar.vue";
import OnlineFriendsVue from "./components/OnlineFriends.vue";

export default {
  name: "App",
  data() {
    return {
      friends: [
        { name: "A", online: true },
        { name: "B", online: true },
        { name: "C", online: false },
        { name: "D", online: true },
        { name: "E", online: false },
      ],
    };
  },
  components: {
    AllFriendsVue,
    NavbarVue,
    OnlineFriendsVue,
  },
  methods: {
    deleteFriend(payload) {
      this.friends = this.friends.filter((friend) => {
        return friend.name != payload.name;
      });
    },
  },
};
</script>

<template>
  <AllFriendsVue :friends="friends" @delete="deleteFriend"></AllFriendsVue>
  <OnlineFriendsVue :friends="friends"></OnlineFriendsVue>
</template>
