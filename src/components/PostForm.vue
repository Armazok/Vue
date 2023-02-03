<template>
<!--  v-bind:value="post.title"-->
<!--  @input="post.title = $event.target.value"-->
<!--           ===          -->
<!--  v-model="post.title"-->



<!--  v-bind:value="post.body"-->
<!--  @input="post.body = $event.target.value"-->
  <!--           ===          -->
  <!--  v-model="post.body"-->


  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input
        v-model="post.title"
        type="text" class="input" placeholder="Название">
    <input
        v-model="post.body"
        type="text" class="input" placeholder="Описание">
    <button class="btn" @click="createPost">Создать</button>
  </form>

</template>

<script>
export default {
  data() {
    return{
      post: {
        title: '',
        body: ''
      }
    }
  },
  methods: {
    createPost(event){
      // event.stopPropagation()
      // event.preventDefault()
      // @submit.prevent
      this.post.id = Date.now()
      this.$emit('create', this.post)
      this.post = {
        title: '',
        body: ''
      }
    }
  }
}
</script>

<style scoped>

</style>










