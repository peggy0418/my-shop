<template>
  <section class="bg-gray-100">
    <div class="max-w-5xl mx-auto px-4 py-8">
      <!-- 標題 -->
      <h2
        class="relative text-xl font-bold mb-5 pl-8 before:content-[''] before:absolute before:left-0 before:top-1/2 before:-translate-y-1/2 before:w-5 before:h-[2px] before:bg-blue-600"
      >
        最新消息
      </h2>

      <!-- News List -->
      <ul class="border-gray-300">
        <li v-for="item in newsList" :key="item.id" class="border-gray-200">
          <div
            class="flex flex-col sm:flex-row sm:items-center gap-2 sm:gap-6 py-1 hover:bg-gray-50 transition"
          >
            <!-- 日期（不可點） -->
            <time class="text-sm text-gray-500 shrink-0 w-32">
              {{ formatDate(item.date) }}
            </time>

            <!-- 標題（可點） -->
            <a :href="item.link" class="text-sm sm:text-base text-blue-700">
              {{ item.title }}
            </a>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const newsList = ref([
  {
    id: 1,
    date: "2026-01-13",
    title: "《光が死んだ夏》動畫化紀念活動即將開始！",
    link: "#",
  },
  {
    id: 2,
    date: "2026-01-02",
    title: "《EVA 30 週年》紀念商品開放預購",
    link: "#",
  },
  {
    id: 3,
    date: "2025-12-27",
    title: "《機動戰士鋼彈》新系列相關商品發售公告",
    link: "#",
  },
  {
    id: 4,
    date: "2025-12-27",
    title: "《機動戰士鋼彈》新系列相關商品發售公告",
    link: "#",
  },
]);

const formatDate = (dateStr) => {
  const d = new Date(dateStr);

  const y = d.getFullYear();
  const m = String(d.getMonth() + 1).padStart(2, "0");
  const day = String(d.getDate()).padStart(2, "0");

  return `${y}.${m}.${day}`;
};
</script>
