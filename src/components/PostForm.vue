<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input v-model="post.title" type="text" placeholder="Название поста">
    <input v-model="post.body" type="text" placeholder="Описание поста">
    <button @click="createPost">Создание поста</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  }
}
</script>

<style scoped>

</style>