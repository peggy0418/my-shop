<template>
  <div class="border-b border-gray-200 bg-gray-100">
    <div
      class="flex justify-between items-center max-w-270 mx-auto h-auto box-border text-xs py-2 px-2 relative"
    >
      <!-- Logo -->
      <div class="logo_area">
        <div class="logo_box max-w-[70px] md:max-w-[140px]">
          <img src="../assets/logo.png" alt="" class="w-full h-auto" />
        </div>
      </div>

      <!-- Desktop Right Items -->
      <div class="hidden lg:flex items-center gap-5">
        <a href="#" class="text-gray-topbar">註冊</a>
        <div class="relative">
          <a href="#" class="text-gray-topbar">最新消息</a>
          <span
            class="absolute -top-2 -right-2.5 bg-red-500 text-white text-[10px] w-4 h-4 flex items-center justify-center rounded-full"
          >
            N
          </span>
        </div>
        <a href="#" class="text-gray-topbar">FAQ</a>
        <Menu />
        <select class="border border-gray-300 h-6 text-xs px-1 bg-white">
          <option>日本語</option>
          <option>English</option>
          <option>中文</option>
        </select>
      </div>

      <!-- Mobile Hamburger -->
      <div class="lg:hidden">
        <button @click="mobileOpen = true" class="p-1 border rounded">
          <span class="material-symbols-outlined text-xl">menu</span>
        </button>

        <!-- Overlay -->
        <div
          v-if="mobileOpen"
          class="fixed inset-0 bg-black/40 z-40"
          @click="mobileOpen = false"
        ></div>

        <!-- Mobile Slide Menu -->
        <transition name="slide">
          <div
            v-if="mobileOpen"
            class="fixed top-0 right-0 h-full w-64 bg-white shadow-lg z-50 flex flex-col gap-3 py-4"
          >
            <!-- Close Button -->
            <button
              @click="mobileOpen = false"
              class="self-end mb-4 p-1 border rounded mr-2"
            >
              <span class="material-symbols-outlined text-xl">X</span>
            </button>

            <!-- 語言選擇 -->
            <select class="border border-gray-300 h-6 text-xs px-1 bg-white w-full">
              <option>日本語</option>
              <option>English</option>
              <option>中文</option>
            </select>

            <!-- 搜尋框 -->
            <div class="w-full my-2">
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
                  class="h-full grow w-auto text-xs px-1 outline-none placeholder-gray-400"
                />
              </div>
            </div>

            <!-- 手機選單內容 -->
            <div class="px-2 flex flex-col gap-2">
              <div>
                <button
                  @click="toggleMobileSub('新品')"
                  class="w-full text-left flex justify-between items-center text-gray-topbar"
                >
                  新品
                  <span class="material-symbols-outlined">
                    {{
                      openMobileSub["新品"] ? "keyboard_arrow_down" : "keyboard_arrow_up"
                    }}
                  </span>
                </button>
                <transition name="slide-down">
                  <div
                    v-show="openMobileSub['新品']"
                    class="overflow-hidden flex flex-col gap-1 mt-1"
                  >
                    <KanaMegaMenu :key="'mega1-mobile'" />
                  </div>
                </transition>
              </div>
              <!-- 書籍 下拉 -->
              <div>
                <button
                  @click="toggleMobileSub('書籍')"
                  class="w-full text-left flex justify-between items-center text-gray-topbar"
                >
                  書籍
                  <span class="material-symbols-outlined">
                    {{
                      openMobileSub["書籍"] ? "keyboard_arrow_down" : "keyboard_arrow_up"
                    }}
                  </span>
                </button>
                <transition name="slide-down">
                  <div
                    v-show="openMobileSub['書籍']"
                    class="overflow-hidden flex flex-col gap-1 mt-1"
                  >
                    <KanaMegaMenu :key="'mega2-mobile'" />
                  </div>
                </transition>
              </div>
              <!-- 其他不展開 -->
              <a href="#" class="text-gray-topbar">CD・BD</a>
              <a href="#" class="text-gray-topbar">角色周邊</a>
              <a href="#" class="text-gray-topbar">活動</a>

              <!-- 帳號相關 -->
              <a href="#" class="text-gray-topbar">註冊</a>
              <a href="#" class="text-gray-topbar">我的主頁</a>
              <div class="relative">
                <a href="#" class="text-gray-topbar">最新消息</a>
                <span
                  class="absolute top-0 left-[20%] bg-red-500 text-white text-[10px] w-4 h-4 flex items-center justify-center rounded-full"
                >
                  N
                </span>
              </div>
              <a href="#" class="text-gray-topbar">FAQ</a>
            </div>
          </div>
        </transition>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive } from "vue";
import Menu from "./Menu.vue";
import KanaMegaMenu from "./KanaMegaMenu_mb.vue";

const mobileOpen = ref(false);
const openMobileSub = reactive({
  新品: false,
  書籍: false,
});

function toggleMobileSub(key) {
  openMobileSub[key] = !openMobileSub[key];
}
</script>
