<template>
  <div class="">
    <h3>Список пользователей</h3>
    <post-item v-for="post in posts" :post="post" :key="post.id" />
  </div>
</template>

<script>
import PostItem from "./PostItem.vue";
export default {
  components: { PostItem },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.post {
  margin-top: 15px;
  padding: 15px;
  border: 2px solid teal;
}
</style>