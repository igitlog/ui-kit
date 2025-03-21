<template>
  <div>
    <h2 class="text-xl font-semibold mb-2">Tooltip Demo</h2>
    <Tooltip text="This is a tooltip!">
      <BaseButton>Hover over me</BaseButton>
    </Tooltip>
  </div>
</template>

<script setup lang="ts">
import Tooltip from '../../components/base/Tooltip.vue';
import BaseButton from '../../components/base/BaseButton.vue';
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 