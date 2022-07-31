<template lang="">
  <h1>Online Friends List</h1>
  <div v-for="(friend, i) in friends">
    <h1 v-if="friend.online == true">{{ friend.name }}</h1>
  </div>
</template>
<script>
export default {
  name: "OnlineFriends",
  props: ["friends"],
  data: function () {
    return {};
  },
};
</script>
<style lang=""></style>
