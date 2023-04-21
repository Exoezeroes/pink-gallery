<script setup>
import AboutHeroTitle from "./About/AboutHeroTitle.vue";
</script>

<template>
  <div
    class="h-screen max-h-[768px] bg-[url('../storage/images/hero-image.jpg')] bg-fixed bg-right bg-no-repeat 2xl:bg-top"
  >
    <div class="grid h-full place-items-center content-center">
      <AboutHeroTitle text="Pink Gallery" />
    </div>
  </div>
</template>
