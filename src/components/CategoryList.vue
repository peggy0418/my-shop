<template>
  <div class="grid grid-cols-2 md:grid-cols-5 gap-4 mb-8">
    <div
      v-for="cat in categories"
      :key="cat"
      class="bg-gray-100 text-center py-4 rounded hover:bg-gray-200 cursor-pointer"
    >
      {{ cat }}
    </div>
  </div>
</template>

<script setup>
const categories = [
  "動畫周邊",
  "書籍",
  "CD/Blu-ray",
  "模型/手辦",
  "活動情報",
];
</script>