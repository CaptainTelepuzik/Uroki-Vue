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

</style>