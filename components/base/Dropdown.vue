<template>
  <div class="relative">
    <button @click="toggle" class="bg-blue-500 text-white py-2 px-4 rounded">
      {{ selected || 'Select' }}
      <ul v-if="isOpen" class="absolute left-0 top-0 bg-white border rounded shadow-lg mt-1">
        <li v-for="option in options" :key="option" @click="select(option)" class="py-2 px-4 hover:bg-gray-200 cursor-pointer text-black">
          {{ option }}
        </li>
      </ul>
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref, defineProps } from 'vue';

const props = defineProps<{
  options: string[];
}>();

const isOpen = ref(false);
const selected = ref('');

const toggle = () => {
  isOpen.value = !isOpen.value;
};

const select = (option: string) => {
  selected.value = option;
  isOpen.value = false;
};
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style> 