<script setup>
import Container from "./Container.vue";
import Card from "./Card.vue";

const data = [
  {
    id: 1,
    username: "sanazbahmanii",
    url: "https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png",
    caption: "Heyyy!",
  },
  {
    id: 2,
    username: "solmazbahmanii",
    url: "https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png",
    caption: "Hello Guys!",
  },
];
</script>

<template>
  <Container>
    <div class="timeline-container">
      <Card v-for="post in data" :key="post.id" :post="post" />
    </div>
  </Container>
</template>

<style scoped>
.timeline-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px 0;
}
</style>
