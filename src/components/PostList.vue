<template>
  <div class="post" v-for="post in posts">
    <p>Название: <span>{{ post.title }}</span> </p>
    <p>Описание: <span>{{ post.body }}</span> </p>
  </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    }
  }

}
</script>

<style scoped>
.post {
  margin-bottom: 1rem;
  border: 2px solid green;
  padding: 15px;
}
</style>