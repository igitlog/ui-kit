<template>
  <button
    :class="['bg-blue-500 text-white font-bold py-2 px-4 rounded', buttonClass]"
    @click="$emit('click')"
  >
    <slot></slot>
  </button>
</template>

<script setup lang="ts">
defineProps<{
  buttonClass?: string; // Позволяет передавать дополнительные классы для стилизации
}>();
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 