<template lang="">
  <h1>Online Friends List</h1>
  <div v-for="(friend, i) in friends">
    <h1 v-if="friend.online == true">{{ friend.name }}</h1>
  </div>
</template>
<script>
export default {
  name: "OnlineFriends",
  data: function () {
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
<style lang=""></style>
