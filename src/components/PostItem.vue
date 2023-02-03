<template>
  <div class="post">
    <div>
      <div><strong>Название:</strong>{{post.title}}</div>
      <div><strong>Описание:</strong>{{post.body}}</div>
    </div>
    <div class="post__btns">
      <button>X</button>
    </div>

  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      require: true
    }
  }
}
</script>

<style scoped>

</style>