<script setup>
import { gradientBgPurplePink } from "@/colors";
import { ref } from "vue";

const isLoaded = ref(false);
</script>

<template>
  <a
    target="_blank"
    class="fixed bottom-6 right-6"
    href="https://wa.me/6281340145484?text=Halo%20Pink%20Gallery%2C"
  >
    <section
      :class="gradientBgPurplePink"
      class="aspect-square w-14 rounded-xl outline outline-gray-100/20"
    >
      <img
        v-show="isLoaded"
        @load="isLoaded = true"
        class="w-full rounded-xl hover:bg-slate-900/25"
        src="/storage/images/whatsapp.png"
      />
    </section>
  </a>
</template>
