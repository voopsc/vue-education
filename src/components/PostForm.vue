<template>
  <form @submit.prevent class="main-form">
    <input type="text"
           placeholder="Post title"
           v-model="post.title"
    >
    <input type="text"
           placeholder="Post description"
           v-model="post.body"
    >
    <button @click="createPost">Create</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: '',
        body: '',
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit('create', this.post);
      this.post = {
        title: '',
        body: '',
      }
    }
  }
}
</script>

<style scoped>
.main-form {
  margin-bottom: 1rem;
  display: flex;
}

.main-form button {
  background: beige;
}
</style>