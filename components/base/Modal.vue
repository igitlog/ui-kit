<template>
  <div v-if="isOpen" class="fixed inset-0 flex items-center justify-center bg-black bg-opacity-50">
    <div class="bg-white rounded-lg p-4">
      <slot></slot>
      <button @click="close" class="mt-4 bg-blue-500 text-white py-2 px-4 rounded">Close</button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps, defineEmits } from 'vue';

const props = defineProps<{
  isOpen: boolean;
}>();

const emit = defineEmits<{
  (e: 'close'): void; // Определяем событие close
}>();

const close = () => {
  emit('close'); // Вызываем событие close
};
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 