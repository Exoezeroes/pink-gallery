<script setup>
import { Head } from "@inertiajs/vue3";
import LayoutGuest from "@/Layouts/LayoutGuest.vue";
import SectionHero from "@/Components/SectionHero.vue";
import SectionMain from "@/Components/SectionMain.vue";
import GoogleMap from "@/Components/GoogleMap.vue";
</script>

<template>
  <LayoutGuest>
    <Head title="Tentang" />
    <SectionHero />
    <SectionMain>
      <div class="mt-12">
        <h1 class="text-center text-4xl font-semibold">
          <span class="text-5xl font-bold text-pink-400 dark:text-pink-500">Pink Gallery</span>
          <br />adalah toko pakaian dan kebutuhan lainnya <br />di <span class="text-green-400 dark:text-emerald-400">Singkawang</span>
        </h1>
      </div>
      <GoogleMap />
    </SectionMain>
  </LayoutGuest>
</template>
