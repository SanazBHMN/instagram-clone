<script setup>
import { ref } from "vue";
import { RouterLink } from "vue-router";
import Container from "./Container.vue";

const searchUserName = ref();

const onSearch = () => {};
</script>

<template>
  <a-layout-header>
    <Container>
      <div class="nav-container">
        <div class="right-content">
          <RouterLink to="/">Instagram</RouterLink>
          <a-input-search
            v-model:value="searchUserName"
            placeholder="username..."
            style="width: 200px"
            @search="onSearch"
          />
        </div>
        <div class="left-content">
          <a-button type="primary">Sign up</a-button>
          <a-button type="primary">Login</a-button>
        </div>
      </div>
    </Container>
  </a-layout-header>
</template>

<style scoped>
.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.right-content {
  display: flex;
  align-items: center;
}

.right-content a {
  margin-right: 10px;
}

.left-content button {
  margin-left: 10px;
}
</style>
