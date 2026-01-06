<template>
  <header class="hidden lg:block border-b border-gray-200 bg-white relative">
    <div class="flex max-w-270 mx-auto items-center gap-8">
      <nav class="flex gap-6 text-sm text-gray-700">
        <!-- 新品 下拉 -->
        <div class="relative group">
          <a class="nav-link flex items-center gap-1">
            新品
            <DownArrow />
          </a>

          <!-- 下拉選單 -->
          <div
            class="hidden lg:block absolute left-0 top-full bg-white border-t border-gray-200 opacity-0 pointer-events-none translate-y-1 transition-all duration-200 ease-out z-50 min-w-full group-hover:opacity-100 group-hover:pointer-events-auto group-hover:translate-y-0"
          >
            <KanaMegaMenu :key="'mega1'" />
          </div>
        </div>

        <!-- 書籍 下拉 -->
        <div class="relative group">
          <a class="nav-link flex items-center gap-1">
            書籍
            <DownArrow />
          </a>

          <div
            class="hidden lg:block absolute -left-[200%] top-full bg-white border-t border-gray-200 opacity-0 pointer-events-none translate-y-1 transition-all duration-200 ease-out z-50 min-w-full group-hover:opacity-100 group-hover:pointer-events-auto group-hover:translate-y-0"
          >
            <KanaMegaMenu :key="'mega2'" />
          </div>
        </div>

        <!-- 其他不展開 -->
        <a class="nav-link">CD・BD</a>
        <a class="nav-link">角色周邊</a>
        <a class="nav-link">活動</a>
      </nav>

      <!-- 搜尋框 -->
      <div class="ml-auto flex items-center">
        <div
          class="flex items-center h-8 border border-gray-300 bg-white focus-within:border-blue-600 transition"
        >
          <span class="px-2 text-gray-500">
            <svg class="w-4 h-4" viewBox="0 0 20 20" fill="currentColor">
              <path
                fill-rule="evenodd"
                d="M8.5 3.5a5 5 0 103.94 8.09l3.48 3.48a.75.75 0 101.06-1.06l-3.48-3.48A5 5 0 008.5 3.5zm-3.5 5a3.5 3.5 0 117 0 3.5 3.5 0 01-7 0z"
                clip-rule="evenodd"
              />
            </svg>
          </span>
          <input
            type="text"
            placeholder="商品搜尋"
            class="h-full w-40 text-sm px-1 outline-none placeholder-gray-400"
          />
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import KanaMegaMenu from "./KanaMegaMenu.vue";

/* 下拉箭頭 */
const DownArrow = {
  template: `
    <svg class="w-3 h-3 text-current" viewBox="0 0 20 20" fill="currentColor">
      <path
        fill-rule="evenodd"
        d="M5.23 7.21a.75.75 0 011.06.02L10 10.94l3.71-3.71a.75.75 0 111.06 1.06l-4.24 4.24a.75.75 0 01-1.06 0L5.21 8.29a.75.75 0 01.02-1.08z"
        clip-rule="evenodd"
      />
    </svg>
  `,
};
</script>
