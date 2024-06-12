<script setup>
import { ref } from "vue";
import { RouterLink, useRouter } from "vue-router";
import Container from "./Container.vue";
import AuthModal from "./AuthModal.vue";

const router = useRouter();
const searchUserName = ref("");
const isAuthenticated = ref(false);

const onSearch = () => {
  if (searchUserName.value) {
    router.push(`/profile/${searchUserName.value}`);
    searchUserName.value = "";
  }
};
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
        <div v-if="!isAuthenticated" class="left-content">
          <AuthModal :isLoggedIn="false" />
          <AuthModal :isLoggedIn="true" />
        </div>
        <div v-else class="left-content">
          <a-button type="primary">Profile</a-button>
          <a-button type="primary">Logout</a-button>
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

.left-content {
  display: flex;
  align-items: center;
}

.left-content button {
  margin-left: 10px;
}
</style>
