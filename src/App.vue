<template>
  <div class="min-h-screen bg-white text-gray-800">
    <Navbar />
    <Hero />
    <div class="container mx-auto px-4 py-8">
      <CategoryList />
      <ProductGrid />
    </div>
    <Footer />
    <div class="bg-red-500 text-white p-4">Tailwind OK</div>
  </div>
</template>

<script setup>
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import CategoryList from "./components/CategoryList.vue";
import ProductGrid from "./components/ProductGrid.vue";
import Footer from "./components/Footer.vue";
</script>
