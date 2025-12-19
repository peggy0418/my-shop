<template>
  <header class="border-b border-gray-200 bg-white">
    <div class="max-w-[1200px] mx-auto h-14 flex items-center gap-8 px-2">
      <div class="text-lg font-bold text-blue-600">animate</div>

      <nav class="flex gap-6 text-sm text-gray-700">
        <a class="hover:text-blue-600">新品</a>
        <a class="hover:text-blue-600">書籍</a>
        <a class="hover:text-blue-600">CD・BD</a>
        <a class="hover:text-blue-600">角色周邊</a>
        <a class="hover:text-blue-600">活動</a>
      </nav>

      <div class="ml-auto flex items-center gap-1">
        <input
          class="border border-gray-300 h-8 px-2 text-sm w-44"
          placeholder="商品搜尋"
        />
        <button class="bg-blue-600 text-white h-8 px-3 text-sm">搜尋</button>
      </div>
    </div>
  </header>
</template>

<script setup>
const menu = ["新品", "書籍", "CD・BD", "角色周邊", "活動"];
</script>
