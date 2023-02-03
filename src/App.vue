<template>
  <div class="app">
    <post-form
        @create="createPost"
    />
    <post-list
        :posts="posts"
    />
  </div>
</template>


<script>
import PostList from "@/Components/PostList.vue";
import PostForm from "@/Components/PostForm.vue";

export default {
  components: {
    PostList, PostForm
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'JS', body: "Описание поста"},
        {id: 2, title: 'CSS', body: "Описание поста"},
        {id: 3, title: 'REACT', body: "Описание поста"},
        {id: 4, title: 'REACT', body: "Описание поста"},
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post)
      console.log(post)
    },
  }
}
</script>


<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}


</style>