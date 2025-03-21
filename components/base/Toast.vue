<template>
  <div v-if="isVisible" class="fixed bottom-4 right-4 bg-blue-500 text-white p-4 rounded">
    {{ message }}
    <button @click="close" class="ml-4">Close</button>
  </div>
</template>

<script setup lang="ts">
import { ref, defineProps } from 'vue';

const props = defineProps<{
  message: string;
}>();

const isVisible = ref(true);

const close = () => {
  isVisible.value = false;
};
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 