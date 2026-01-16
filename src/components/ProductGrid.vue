<template>
  <div class="max-w-270 mx-auto px-2">
    <!-- 標題 -->
    <h2
      class="relative text-xl font-bold mb-5 pl-8 before:content-[''] before:absolute before:left-0 before:top-1/2 before:-translate-y-1/2 before:w-5 before:h-[2px] before:bg-blue-600"
    >
      隨機商品
    </h2>
    <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-3">
      <div
        v-for="p in products"
        :key="p.id"
        class="border border-gray-200 p-2 hover:shadow-sm transition"
      >
        <img :src="p.image" class="w-full aspect-[3/4] object-cover mb-2" />

        <p class="text-xs leading-tight line-clamp-2 mb-1 text-gray-800">
          {{ p.name }}
        </p>

        <p class="text-sm font-bold text-blue-600">
          {{ p.price }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
const products = [
  {
    id: 1,
    name: "角色壓克力立牌",
    price: "¥1,320",
    image: "https://picsum.photos/300/400",
  },
  {
    id: 2,
    name: "限定版漫畫 第1卷",
    price: "¥2,200",
    image: "https://picsum.photos/300/400",
  },
  {
    id: 3,
    name: "角色徽章組",
    price: "¥880",
    image: "https://picsum.photos/300/400",
  },
  {
    id: 4,
    name: "PVC 完成品模型",
    price: "¥6,800",
    image: "https://picsum.photos/300/400",
  },
];
</script>
