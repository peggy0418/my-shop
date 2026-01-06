<script setup>
import { ref, computed } from "vue";

/* 注音大分類 */
const bopomofoTabs = ["ㄅ", "ㄆ", "ㄇ", "ㄈ", "ㄉ", "ㄊ", "ㄋ", "ㄌ"];

/* 子分類 */
const subMap = {
  ㄅ: ["ㄅ", "ㄆ", "ㄇ", "ㄈ"],
  ㄉ: ["ㄉ", "ㄊ", "ㄋ", "ㄌ"],
};

/* 狀態 */
const activeTab = ref("ㄅ");
const activeBopomofo = ref("ㄅ");

/* 商品資料（範例） */
const products = {
  ㄅ: ["寶可夢", "白貓 Project", "BanG Dream!", "BLEACH 死神", "不滅之火", "白沙屯媽祖"],
  ㄆ: ["排球少年", "霹靂布袋戲"],
  ㄇ: ["名偵探柯南", "魔法少女小圓"],
  ㄈ: ["鋼之鍊金術師", "風之谷"],
};

const list = computed(() => products[activeBopomofo.value] || []);
</script>

<template>
  <div class="w-full p-0 lg:w-270 lg:p-6">
    <!-- 注音大分類 (桌面版才顯示) -->
    <div class="hidden lg:flex border-b mb-4">
      <button
        v-for="tab in bopomofoTabs"
        :key="tab"
        @mouseenter="
          activeTab = tab;
          activeBopomofo = subMap[tab]?.[0];
        "
        class="px-6 py-2 text-sm border-b-2 transition"
        :class="
          activeTab === tab
            ? 'border-blue-600 text-blue-600'
            : 'border-transparent text-gray-600 hover:text-blue-600'
        "
      >
        {{ tab }}
      </button>
    </div>

    <!-- 注音子分類 (桌面版才顯示) -->
    <div class="hidden lg:flex gap-2 mb-6">
      <button
        v-for="bpmf in subMap[activeTab]"
        :key="bpmf"
        @mouseenter="activeBopomofo = bpmf"
        class="px-4 py-1 border text-sm transition"
        :class="
          activeBopomofo === bpmf
            ? 'bg-blue-600 text-white border-blue-600'
            : 'hover:border-blue-600 hover:text-blue-600'
        "
      >
        {{ bpmf }}
      </button>
    </div>

    <!-- 商品列表（三欄，手機可滾動） -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-x-10">
      <a
        v-for="item in list"
        :key="item"
        href="#"
        class="group flex justify-between items-center py-2 border-b text-sm hover:text-blue-600"
      >
        {{ item }}
        <span class="opacity-0 group-hover:opacity-100 transition">›</span>
      </a>
    </div>
  </div>
</template>
