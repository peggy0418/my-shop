<template>
  <Swiper
    :modules="[Autoplay, Pagination, Navigation]"
    :slides-per-view="1"
    :loop="true"
    :autoplay="{ delay: 4000 }"
    :pagination="{ clickable: true }"
    navigation
    class="max-w-[810px] w-100% h-auto"
  >
    <!-- Slide 1 -->
    <SwiperSlide>
      <div class="relative w-full h-full">
        <img src="../assets/pokemon.jpg" class="w-full h-full object-cover" />
        <div class="absolute inset-0 flex items-center justify-center">
          <!-- <h1 class="text-4xl font-bold text-white drop-shadow-lg">
            歡迎來到 Animate Shop
          </h1> -->
        </div>
      </div>
    </SwiperSlide>

    <!-- Slide 2 -->
    <SwiperSlide>
      <div class="relative w-full h-full">
        <img src="../assets/pjsk.jpg" class="w-full h-full object-cover" />
        <div class="absolute inset-0 flex items-center justify-center">
          <!-- <h1 class="text-4xl font-bold text-white drop-shadow-lg">限定商品販售中</h1> -->
        </div>
      </div>
    </SwiperSlide>
  </Swiper>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination, Navigation } from "swiper/modules";

import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";
</script>
