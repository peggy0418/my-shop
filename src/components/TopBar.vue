<template>
  <div class="border-b border-gray-200 bg-white">
    <div class="max-w-[1200px] mx-auto h-9 flex items-center text-xs text-gray-600 px-2">
      <!-- Left -->
      <div class="flex gap-3 items-center justify-between">
        <div class="logo_area">
          <div class="logo_box max-w-[165px]">
            <img src="../assets/logo.png" alt="" class="w-full h-auto" />
          </div>
        </div>
        <div class="flex gap-1 items-center">
          <a href="#" class="hover:text-blue-600"> English Page </a>
          <span class="text-gray-300">/</span>
          <a href="#" class="hover:text-blue-600"> 中文购买说明 </a>
        </div>
      </div>

      <!-- Right -->
      <div class="ml-auto flex items-center gap-4">
        <a href="#" class="hover:text-blue-600"> 新規會員登錄 </a>
        <a href="#" class="hover:text-blue-600"> マイページ </a>

        <div class="relative">
          <a href="#" class="hover:text-blue-600"> お知らせ </a>
          <span
            class="absolute -top-1 -right-2 bg-red-500 text-white text-[10px] w-4 h-4 flex items-center justify-center rounded-full"
          >
            N
          </span>
        </div>

        <a href="#" class="hover:text-blue-600"> FAQ </a>

        <!-- Language -->
        <select class="border border-gray-300 h-6 text-xs px-1 bg-white">
          <option>日本語</option>
          <option>English</option>
          <option>中文</option>
        </select>
      </div>
    </div>
  </div>
</template>
