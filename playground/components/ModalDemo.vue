<template>
  <div>
    <h2 class="text-xl font-semibold mb-2">Modal Demo</h2>
    <BaseButton @click="openModal">Open Modal</BaseButton>
    <Modal :isOpen="isModalOpen" @close="isModalOpen = false">
      <h3 class="text-lg">This is a modal!</h3>
      <p>Content goes here.</p>
    </Modal>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import BaseButton from '../../components/base/BaseButton.vue';
import Modal from '../../components/base/Modal.vue';

const isModalOpen = ref(false);

const openModal = () => {
  isModalOpen.value = true;
};
</script>

<style scoped>
/* Добавьте стили, если необходимо */
</style>