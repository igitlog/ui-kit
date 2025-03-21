<template>
  <div class="container mx-auto p-4">
    <h1 class="text-2xl font-bold mb-4">UI Kit Playground</h1>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
      <div class="demo-tile">
        <ModalDemo />
      </div>
      <div class="demo-tile">
        <DropdownDemo />
      </div>
      <div class="demo-tile">
        <TabsDemo />
      </div>
      <div class="demo-tile">
        <AccordionDemo />
      </div>
      <div class="demo-tile">
        <ToastDemo />
      </div>
      <div class="demo-tile">
        <TooltipDemo />
      </div>
      <div class="demo-tile">
        <CardDemo />
      </div>
      <div class="demo-tile">
        <LoaderDemo />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import ModalDemo from './components/ModalDemo.vue';
import DropdownDemo from './components/DropdownDemo.vue';
import TabsDemo from './components/TabsDemo.vue';
import AccordionDemo from './components/AccordionDemo.vue';
import ToastDemo from './components/ToastDemo.vue';
import TooltipDemo from './components/TooltipDemo.vue';
import CardDemo from './components/CardDemo.vue';
import LoaderDemo from './components/LoaderDemo.vue';
</script>

<style>
.demo-tile {
  padding: 16px; /* Отступы вокруг плитки */
  background-color: #943d3d; /* Цвет фона плитки */
  border-radius: 8px; /* Закругление углов */
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Тень для плитки */
}
</style> 