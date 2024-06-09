<script setup>
import { ref, defineProps } from "vue";

const props = defineProps(["isLoggedIn"]);

const title = props.isLoggedIn ? "Login" : "Sign Up";

const open = ref(false);

const showModal = () => {
  open.value = true;
};

const handleOk = (e) => {
  console.log(e);
  open.value = false;
};
</script>

<template>
  <div>
    <a-button type="primary" @click="showModal" class="btn">{{
      title
    }}</a-button>
    <a-modal v-model:open="open" :title="title" @ok="handleOk">
      <a-input
        v-if="!isLoggedIn"
        v-model:value="value"
        placeholder="Username"
        class="input"
      />
      <a-input v-model:value="value" placeholder="Email" class="input" />
      <a-input v-model:value="value" placeholder="Password" class="input" />
    </a-modal>
  </div>
</template>

<style scoped>
.btn {
  margin-left: 10px;
}

.input {
  margin-top: 5px;
}
</style>
