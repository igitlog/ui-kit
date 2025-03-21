<template>
  <div class="relative inline-block">
    <slot></slot>
    <div v-if="isVisible" class="absolute bg-gray-700 text-white p-2 rounded">
      {{ text }}
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, defineProps } from 'vue';

const props = defineProps<{
  text: string;
}>();

const isVisible = ref(false);
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 