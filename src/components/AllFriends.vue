<template lang="">
  <h1>All friends list</h1>
  <div v-for="(friend, i) in friends" :key="i">
    <h1>{{ friend.name }}</h1>
  </div>
</template>
<script>
export default {
  name: "AllFriends",
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
};
</script>
<style>
* {
  text-align: center;
}
</style>
