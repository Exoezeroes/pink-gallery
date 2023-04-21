<script setup>
import { Head } from "@inertiajs/vue3";
import AboutHeader from "@/Components/About/AboutHeader.vue";
import AboutBestItems from "@/Components/About/AboutBestItems.vue";
import LayoutGuest from "@/Layouts/LayoutGuest.vue";
import SectionHero from "@/Components/SectionHero.vue";
import SectionMain from "@/Components/SectionMain.vue";
import GoogleMap from "@/Components/GoogleMap.vue";
import SectionFooter from "@/Components/SectionFooter.vue";
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
    <SectionFooter>
      <div class="py-6 bg-slate-900">
        <div class="grid place-items-center">
          &copy; 2018 - {{ new Date().getFullYear() }} Pink Gallery
        </div>
      </div>
    </SectionFooter>
  </LayoutGuest>
</template>
