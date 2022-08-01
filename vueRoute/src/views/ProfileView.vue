<template lang="">
  <div>
    <h1>This is Profile page for: {{ user_id }}</h1>
    <button @click="contact">Contact</button>
    <button @click="home">Home</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      user_id: this.$route.params.id,
    };
  },
  methods: {
    updateId() {
      this.user_id = this.$route.params.id;
    },
    contact() {
      this.$router.push({ name: "contact" });
    },
    home() {
      this.$router.push({ name: "home" });
    },
  },
  watch: {
    $route: "updateId",
  },
};
</script>
<style lang=""></style>
