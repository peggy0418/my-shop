<template>
  <div class="bg-blue-600 my-0 mx-auto">
    <div
      class="bg-blue-600 max-w-270 mx-auto my-0 grid grid-cols-2 items-center md:grid-cols-7 mb-4.25"
    >
      <div
        v-for="cat in categories"
        :key="cat"
        class="bg-blue-600 text-center text-white py-4 border-r-1 border-gray-800 hover:bg-blue-700 cursor-pointer"
      >
        {{ cat }}
      </div>
      <!-- 愛心&購物車 -->
      <div class="hidden lg:flex lg:items-center lg:justify-center lg:gap-1">
        <div
          class="heart_box bg-blue-700 w-[74px] h-[68px] flex items-center justify-center cursor-pointer"
          @mouseenter="hover = true"
          @mouseleave="hover = false"
        >
          <svg
            v-if="hover"
            xmlns="http://www.w3.org/2000/svg"
            fill="red"
            viewBox="0 0 24 24"
            class="w-8 h-8"
          >
            <path
              d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"
            />
          </svg>
          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            stroke="white"
            viewBox="0 0 24 24"
            class="w-8 h-8"
          >
            <path
              d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"
            />
          </svg>
        </div>
        <div
          class="shopping_cart bg-blue-700 grow w-[74px] h-[68px] flex items-center justify-center"
        >
          <span class="material-symbols-outlined text-white"> shopping_cart </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const categories = ["最新商品", "限定版", "最新活動", "排行榜", "特價商品"];

const hover = ref(false); // 一開始是空心愛心
</script>
