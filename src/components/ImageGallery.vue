<script setup>
const props = defineProps(["posts"]);
console.log(props.posts);
</script>

<template>
  <div class="image-gallery-container">
    <img v-for="post in props.posts" :key="post.id" :src="post.image" alt="" />
  </div>
</template>

<style scoped>
.image-gallery-container {
  display: flex;
  justify-content: left;
  flex-wrap: wrap;
}

img {
  margin: 5px;
  width: 200px;
}
</style>
