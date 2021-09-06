<template>
  <div class="home">
    <h1>Home</h1>
    <PostList v-if="posts.length" :posts="posts"/>
    <h3 v-else-if="error">Error loading data</h3>
    <h3 v-else>Loading...</h3>
  </div>
</template>

<script>

import PostList from '../components/PostList.vue';
import getPosts from '../composables/getPosts';

export default {
  name: 'Home',
  components: { PostList },
  setup() {
    const { posts, error, load } = getPosts();

    load();

    return { posts, error };

  },

}
</script>
