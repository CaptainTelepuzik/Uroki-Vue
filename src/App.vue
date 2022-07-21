<template>
  <div class="app">
    <PostForm
        @create ="createPost"
    />
    <PostList
        :posts="posts"

    />
  </div>

</template>

<script>
import PostList from "@/components/PostList";
import PostForm from "@/components/PostForm";

export default {
  name: 'App',
  components:{
    PostForm,
    PostList
  },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "VueHue",
          content: "Описание",
        },
        {
          id: 2,
          title: "VueHue2",
          content: "Описание2",
       },
        {
          id: 3,
          title: "VueHue3",
          content: "Описание3",
        },
      ]
    }
  },
  methods:{
    createPost(post){
      this.posts.push(post);
    }
  }
}
</script>

<style>
#app *{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
