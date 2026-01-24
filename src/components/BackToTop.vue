<template>
  <transition name="fade">
    <button
      v-show="showButton"
      @click="scrollToTop"
      class="fixed bottom-8 right-4 bg-blue-600 text-white w-[30px] md:w-auto h-[30px] md:h-auto p-3 rounded-full shadow-lg hover:bg-blue-700 z-50 flex items-center justify-center space-x-1"
    >
      <span class="text-sm m-0 aspect-1/1 sm:text-lg">↑</span>
      <span class="hidden md:inline">Top</span>
      <!-- 手機版隱藏，sm以上顯示 -->
    </button>
  </transition>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const showButton = ref(false);

const checkScroll = () => {
  showButton.value = window.scrollY > 200;
};

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
};

onMounted(() => {
  window.addEventListener("scroll", checkScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", checkScroll);
});
</script>
