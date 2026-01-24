<template>
  <div class="max-w-270 mx-auto px-2">
    <!-- 標題 -->
    <h2
      class="relative text-xl font-bold mb-16 pl-8 before:content-[''] before:absolute before:left-0 before:top-1/2 before:-translate-y-1/2 before:w-5 before:h-[2px] before:bg-blue-600"
    >
      熱門商品
    </h2>
    <div class="grid grid-cols-2 lg:grid-cols-4 gap-3">
      <div v-for="p in products" :key="p.id">
        <div class="border border-gray-200 p-2 hover:shadow-sm transition relative group">
          <!-- 特典標籤：固定在卡片最上方 -->
          <div
            v-if="p.hasBonus"
            class="absolute -top-10 left-0 bg-white text-blue-600 text-[11px] font-semibold border border-blue-600 px-2 py-1 rounded shadow-md z-10"
          >
            贈送特典
          </div>

          <div class="mb-2 mt-3">
            <!-- 留空間給標籤 -->
            <img :src="p.image" class="w-full aspect-[3/4] object-contain" />
          </div>

          <p class="text-xs leading-tight line-clamp-2 mb-1 text-gray-800">
            {{ p.name }}
          </p>

          <p class="text-sm font-bold text-blue-600">
            {{ p.price }}
          </p>
          <br />
          <div>
            <div>
              商品狀態:
              <span class="text-sm font-bold text-blue-600">
                {{ p.productstate }}
              </span>
            </div>
            <div>
              商品類別:
              <span class="text-sm font-bold text-blue-600">
                {{ p.category }}
              </span>
            </div>
            <div>
              發售日:
              <span class="text-sm font-bold text-blue-600">
                {{ p.date }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import RandomImg from "../assets/random_img.jpg";
const products = [
  {
    id: 1,
    name: "角色壓克力立牌",
    price: "2,200元(含稅)",
    image: RandomImg,
    hasBonus: true, // 有贈送特典
    productstate: "預約中",
    category: "立牌",
    date: "2026/01/22",
  },
  {
    id: 2,
    name: "角色壓克力立牌",
    price: "2,200元(含稅)",
    image: RandomImg,
    hasBonus: true, // 有贈送特典
    productstate: "預約中",
    category: "立牌",
    date: "2026/01/22",
  },
  {
    id: 3,
    name: "角色壓克力立牌",
    price: "2,200元(含稅)",
    image: RandomImg,
    hasBonus: false,
    productstate: "有現貨",
    category: "立牌",
    date: "2026/01/22",
  },
  {
    id: 4,
    name: "角色壓克力立牌",
    price: "2,200元(含稅)",
    image: RandomImg,
    hasBonus: false,
    productstate: "有現貨",
    category: "立牌",
    date: "2026/01/22",
  },
];
</script>
