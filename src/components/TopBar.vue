<template>
  <div class="border-b border-gray-200 bg-gray-100">
    <div class="max-w-270 mx-auto max-h-12 flex items-center text-xs">
      <!-- Left -->
      <div class="flex gap-25 items-center py-2">
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
      <div class="ml-auto flex items-center gap-4">
        <a href="#" class="text-gray-topbar"> 新規會員登錄 </a>
        <a href="#" class="text-gray-topbar"> マイページ </a>

        <div class="relative">
          <a href="#" class="text-gray-topbar"> お知らせ </a>
          <span
            class="absolute -top-1 -right-2 bg-red-500 text-white text-[10px] w-4 h-4 flex items-center justify-center rounded-full"
          >
            N
          </span>
        </div>

        <a href="#" class="text-gray-topbar"> FAQ </a>

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
