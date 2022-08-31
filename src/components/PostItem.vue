<template>
  <div class="post">
    <div><strong>ID:</strong>{{ post.id }}</div>
    <div><strong>Название:</strong>{{ post.title }}</div>
    <div><strong>Описание:</strong>{{ post.body }}</div>
    <MyButton @click="$emit('remove', post)">Удалить</MyButton>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>

</style>