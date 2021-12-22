<template>
  <post-form
      @create="createPost"
  />
  <post-list
      :posts="posts"
  />
</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";

export default {
  components: {
    PostList,
    PostForm
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'Post 1', body: 'Desc 1'},
        {id: 2, title: 'Post 2', body: 'Desc 2'},
        {id: 3, title: 'Post 3', body: 'Desc 3'},
        {id: 4, title: 'Post 4', body: 'Desc 4'},
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },
  }
}
</script>

<style>




</style>