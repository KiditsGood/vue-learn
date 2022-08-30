<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <MyInput v-model="post.title" type="text" placeholder="Название поста" />
    <MyInput v-model="post.body" type="text" placeholder="Описание поста" />
    <MyButton @click="createPost">Создание поста</MyButton>
  </form>
</template>

<script>

import MyInput from "@/components/UI/MyInput";
export default {
  components: {MyInput},
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  },
  methods: {
    createPost() {
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