<template>
  <div>
    <h2 class="text-xl font-semibold mb-2">Toast Demo</h2>
    <BaseButton @click="showToast">Show Toast</BaseButton>
    <Toast v-if="isToastVisible" message="This is a toast message!" />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import BaseButton from '../../components/base/BaseButton.vue';
import Toast from '../../components/base/Toast.vue';

const isToastVisible = ref(false);

const showToast = () => {
  isToastVisible.value = true;
  setTimeout(() => {
    isToastVisible.value = false;
  }, 3000);
};
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 