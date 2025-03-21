<template>
  <div>
    <h2 class="text-xl font-semibold mb-2">Accordion Demo</h2>
    <Accordion :items="items" />
  </div>
</template>

<script setup lang="ts">
import Accordion from '../../components/base/Accordion.vue';

const items = [
  { title: 'Item 1', isOpen: false, content: 'Content for Item 1' },
  { title: 'Item 2', isOpen: false, content: 'Content for Item 2' },
];
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 