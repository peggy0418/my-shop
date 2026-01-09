<template>
  <div class="min-h-screen bg-white text-gray-800">
    <TopBar />
    <Navbar />

    <div class="container mx-auto px-4 py-8">
      <CategoryList />
      <Hero />
      <ProductGrid />
    </div>
    <Footer />
  </div>
</template>

<script setup>
import TopBar from "./components/TopBar.vue";
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import CategoryList from "./components/CategoryList.vue";
import ProductGrid from "./components/ProductGrid.vue";
import Footer from "./components/Footer.vue";
</script>
