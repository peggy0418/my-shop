<template>
  <header
    class="m-2 border-b border-gray-200 bg-white relative lg:m-0 lg:flex lg:flex-wrap lg:max-w-270 lg:mx-auto lg:items-center lg:gap-8 hidden lg:block"
  >
    <nav class="flex gap-6 text-sm text-gray-700">
      <!-- 新品 下拉 -->
      <div class="relative group">
        <a class="nav-link flex items-center gap-1">
          新品
          <DownArrow />
        </a>

        <!-- 下拉選單 -->
        <div
          class="absolute left-0 top-full bg-white border-t border-gray-200 opacity-0 pointer-events-none translate-y-1 transition-all duration-200 ease-out z-50 min-w-full group-hover:opacity-100 group-hover:pointer-events-auto group-hover:translate-y-0"
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
          class="absolute left-[-200%] top-full bg-white border-t border-gray-200 opacity-0 pointer-events-none translate-y-1 transition-all duration-200 ease-out z-50 min-w-full group-hover:opacity-100 group-hover:pointer-events-auto group-hover:translate-y-0"
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
    <div class="flex items-center lg:ml-auto">
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
  </header>
</template>
