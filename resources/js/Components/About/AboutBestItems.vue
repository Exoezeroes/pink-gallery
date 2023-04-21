<script setup>
import { products } from "@/bestProducts";
import AboutBestItem from "@/Components/About/AboutBestItem.vue";
</script>

<template>
  <div class="mt-24">
    <h1 class="text-center text-4xl font-bold text-pink-900 dark:text-pink-200">
      Produk Unggulan Kami
    </h1>
    <div class="mt-6 grid grid-cols-1 place-items-center lg:grid-cols-3 gap-6">
      <AboutBestItem
        v-for="(product, index) in products"
        :key="index"
        :product="product"
      />
    </div>
  </div>
</template>
