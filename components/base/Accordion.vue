<template>
  <div>
    <div v-for="item in localItems" :key="item.title">
      <button @click="toggle(item)" class="w-full text-left py-2 px-4 bg-gray-200">
        {{ item.title }}
      </button>
      <div v-if="item.isOpen" class="p-4 border-b">
        {{ item.content }}
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const props = defineProps<{
  items: { title: string; content: string; isOpen?: boolean }[];
}>();

// Создаём реактивную копию props.items
const localItems = ref(props.items.map(item => ({ ...item, isOpen: item.isOpen ?? false })));

const toggle = (item: { title: string; content: string; isOpen: boolean }) => {
  // Закрываем все элементы, кроме текущего
  localItems.value.forEach(i => {
    i.isOpen = i.title === item.title ? !i.isOpen : false;
  });
};
</script>


<style scoped>
/* Добавьте стили, если необходимо */
</style> 