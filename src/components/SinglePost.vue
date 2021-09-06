<template>
  <div class="post">
    <router-link :to="{ name: 'Details', params: { id: post.id } }">{{ post.title }}</router-link>
    <p>{{ snippet }}</p>
    <span v-for="tag in post.tags" :key="tag">
      #{{ tag }}
    </span>
  </div>
</template>
<script>
import { computed } from 'vue';
  export default {
    props: {
      post: Object
    },

    setup(props) {

      const snippet = computed(() => {
        return props.post.body.substr(0,100) + '....';
      });

      return { snippet };
    }
  }
</script>

<style lang="scss" scoped>

</style>