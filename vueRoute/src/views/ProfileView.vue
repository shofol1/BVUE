<template lang="">
  <div>This is Profile page for: {{ user_id }}</div>
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
  },
  watch: {
    $route: "updateId",
  },
};
</script>
<style lang=""></style>
