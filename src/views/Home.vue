<template>
  <div class="home">
    <h1>Home</h1>
    <PostList :posts="posts"/>
  </div>
</template>

<script>

import PostList from '../components/PostList.vue';
import { ref } from 'vue';

export default {
  name: 'Home',
  components: { PostList },
  setup() {

    const posts = ref([
      { title: 'Welcome to the blog', body: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt, deleniti optio officiis consequatur obcaecati non perspiciatis corporis at dolores mollitia expedita ipsum cum cupiditate rerum tenetur voluptatibus saepe molestias totam neque dignissimos. Earum, aliquid fugit aperiam architecto animi fuga praesentium aspernatur quam, pariatur voluptatibus illo placeat labore necessitatibus enim numquam?', id: 1 },
      { title: 'Top 5 CSS tips', body: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt, deleniti optio officiis consequatur obcaecati non perspiciatis corporis at dolores mollitia expedita ipsum cum cupiditate rerum tenetur voluptatibus saepe molestias totam neque dignissimos. Earum, aliquid fugit aperiam architecto animi fuga praesentium aspernatur quam, pariatur voluptatibus illo placeat labore necessitatibus enim numquam?', id: 2 }
    ]);

    return { posts };
  },
}
</script>
