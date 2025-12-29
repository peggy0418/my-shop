<template>
  <div class="relative" @mouseenter="showMenu = true" @mouseleave="showMenu = false">
    <!-- Menu Icon -->
    <span class="material-symbols-outlined cursor-pointer"> menu </span>

    <!-- Dropdown Menu -->
    <div
      v-show="showMenu"
      class="absolute right-0 w-40 bg-gray-100 border-gray-100 rounded shadow-lg transition-opacity duration-200 z-9999 mt-[-5px]"
    >
      <ul class="flex flex-col">
        <li class="px-4 py-2 hover:bg-gray-100 cursor-pointer">選項 1</li>
        <li class="px-4 py-2 hover:bg-gray-100 cursor-pointer">選項 2</li>
        <li class="px-4 py-2 hover:bg-gray-100 cursor-pointer">選項 3</li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const showMenu = ref(false);
</script>

<style scoped>
/* 可選：讓下拉選單平滑出現 */
[v-cloak] {
  display: none;
}
</style>
