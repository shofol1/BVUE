<template lang="">
  <h1>All friends list</h1>
  <div v-for="(friend, i) in friends" :key="friend.name">
    <h1 @click="remove(friend.name)">
      {{ friend.name }} || {{ friend.online }}
    </h1>
  </div>
</template>
<script>
export default {
  name: "AllFriends",
  props: ["friends"],
  data() {
    return {};
  },
  methods: {
    remove(name) {
      this.$emit("delete", { name });
    },
  },
};
</script>
<style>
* {
  text-align: center;
}
</style>
