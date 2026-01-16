<template>
  <div class="min-h-screen bg-white text-gray-800">
    <TopBar />
    <Navbar />
    <CategoryList />
    <div class="container mx-auto">
      <Hero />
      <Banner_ad />
    </div>
    <NewsList :news="latestNews" />
    <div class="container mx-auto">
      <ProductGrid />
    </div>
    <Footer />
  </div>
</template>

<script setup>
import TopBar from "./components/TopBar.vue";
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import Banner_ad from "./components/Banner_ad.vue";
import CategoryList from "./components/CategoryList.vue";
import ProductGrid from "./components/ProductGrid.vue";
import NewsList from "./components/NewsList.vue";
import Footer from "./components/Footer.vue";
</script>
