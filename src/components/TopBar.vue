<template>
  <div class="border-b border-gray-200 bg-gray-100">
    <div class="max-w-270 mx-auto max-h-12 box-border flex items-center text-xs py-2">
      <!-- Left -->
      <div class="flex gap-15 items-center">
        <div class="logo_area">
          <div class="logo_box max-w-[140px]">
            <img src="../assets/logo.png" alt="" class="w-full h-auto" />
          </div>
        </div>
        <div class="flex gap-2 items-center">
          <a href="#" class="text-gray-topbar leading-4 tracking-wider"> English Page </a>
          <span class="text-base text-gray-topbar">/</span>
          <a href="#" class="text-gray-topbar leading-4 tracking-wider"> 中文購買說明 </a>
        </div>
      </div>

      <!-- Right -->
      <div class="ml-auto flex items-center gap-11 topbar-right">
        <a href="#" class="text-gray-topbar"> 新規會員登錄 </a>
        <a href="#" class="text-gray-topbar"> マイページ </a>

        <div class="relative">
          <a href="#" class="text-gray-topbar"> お知らせ </a>
          <span
            class="absolute -top-2 -right-2.5 bg-red-500 text-white text-[10px] w-4 h-4 flex items-center justify-center rounded-full"
          >
            N
          </span>
        </div>

        <a href="#" class="text-gray-topbar"> FAQ </a>
        <Menu />
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

<script setup>
import Menu from "./Menu.vue";
</script>
