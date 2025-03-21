<template>
  <div>
    <h2 class="text-xl font-semibold mb-2">Dropdown Demo</h2>
    <Dropdown :options="options" />
  </div>
</template>

<script setup lang="ts">
import Dropdown from '../../components/base/Dropdown.vue';

const options = ['Option 1', 'Option 2', 'Option 3'];
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 