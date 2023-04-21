<script setup>
import { Head } from "@inertiajs/vue3";
import AboutHeader from "@/Components/About/AboutHeader.vue";
import AboutBestItems from "@/Components/About/AboutBestItems.vue";
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
      <AboutHeader />
      <GoogleMap />
      <AboutBestItems />
    </SectionMain>
  </LayoutGuest>
</template>
