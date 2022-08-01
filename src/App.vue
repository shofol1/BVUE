<script>
import HookVue from "./components/Hook.vue";
import axios from "axios";

export default {
  name: "App",
  data() {
    return {
      users: [],
      posts: [],
      searchItem: "",
    };
  },
  created() {
    axios
      .get("https://jsonplaceholder.typicode.com/posts")
      .then((res) => (this.posts = res.data))
      .catch((err) => console.log(err));
  },
  components: {
    HookVue,
  },
  computed: {
    filtered() {
      return this.posts.filter((post) => {
        return post.title.match(this.searchItem);
      });
    },
  },
  methods: {},
};
</script>

<template>
  <HookVue></HookVue>
  <input type="text" placeholder="search" v-model="searchItem" />

  <div v-for="(post, i) in filtered" :key="post.id">
    <h1>{{ post.title }}</h1>
    <p>{{ post.body }}</p>
  </div>
</template>
