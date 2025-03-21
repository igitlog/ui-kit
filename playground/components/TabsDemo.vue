<template>
  <div>
    <h2 class="text-xl font-semibold mb-2">Tabs Demo</h2>
    <Tabs :tabs="tabs">
      <template #default="{ selectedTab }">
        <div>{{ selectedTab.content }}</div>
      </template>
    </Tabs>
  </div>
</template>

<script setup lang="ts">
import Tabs from '../../components/base/Tabs.vue';

const tabs = [
  { name: 'Tab 1', content: 'Content for Tab 1' },
  { name: 'Tab 2', content: 'Content for Tab 2' },
  { name: 'Tab 3', content: 'Content for Tab 3' },
  { name: 'Tab 4', content: 'Content for Tab 4' },
];
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 