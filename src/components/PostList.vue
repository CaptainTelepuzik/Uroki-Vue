<template>
<div>
  <h3>Список пользователей</h3>
  <PostItem
      :key = "post.id"
      v-for="post in posts"
      :post="post"
  />
  </div>
</template>

<script>
import PostItem from "@/components/PostItem";
export default {
  name: "PostList",
  components: {
    PostItem
  },
  props:{
    posts:{
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.post{
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
}

</style>