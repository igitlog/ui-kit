<template>
  <div>
    <div class="flex border-b">
      <button
        v-for="tab in tabs"
        :key="tab.name"
        @click="selectTab(tab)"
        :class="['py-2 px-4', { 'border-b-2 border-blue-500': tab === selectedTab }]"
      >
        {{ tab.name }}
      </button>
    </div>
    <div class="p-4">
      <slot :selectedTab="selectedTab" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, defineProps } from 'vue';

const props = defineProps<{
  tabs: { name: string; content: string }[];
}>();

const selectedTab = ref(props.tabs[0]);

const selectTab = (tab: { name: string; content: string }) => {
  selectedTab.value = tab;
};
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 