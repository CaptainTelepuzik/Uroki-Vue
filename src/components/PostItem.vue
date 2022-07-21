<template>
  <div>
    <div class ="post"></div>
    <div>Название:{{post.title}}</div>
    <div>Описание:{{post.content}}</div>
  </div>
</template>

<script>
export default {
  name: "PostItem",
  props:{
    post:{
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.post{
  margin-top: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}


</style>