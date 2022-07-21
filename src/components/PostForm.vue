<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input
    v-model="post.title"
    class="input"
    type="text"
    placeholder="Название">
    <input
        v-model="post.content"
        class="input"
        type="text"
        placeholder="Описание">
    <button
      class="btn"
      @click = "CreatePost"
      >Создать</button>
  </form>
</template>

<script>
export default {
  name: "PostForm",
  methods:{
    createPost(){
      this.post.id = Date.now();
      this.$emit("create", this.post)
    this.post = {
        title: "",
        content: ""
    }
    }
  },
  data(){
    return{
      post:{
        title: "",
        content: ""
      }
    }
  }
}
</script>

<style scoped>

form {
  display: flex;
  flex-direction: column;
}
.btn {
  margin-top: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}

.input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
  margin-top: 15px;
}

</style>