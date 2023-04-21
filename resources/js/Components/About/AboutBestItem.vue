<script setup>
import { gradientBgPurplePink } from "@/colors";

defineProps({
  product: {
    type: Object,
    required: true,
  },
});
</script>

<template>
 <a :href="product.href" target="_blank">
    <div :class="gradientBgPurplePink" class="h-[400px] w-fit rounded">
      <img
        class="h-full rounded-sm object-cover p-1"
        :src="product.src"
        :alt="product.alt"
      />
    </div>
    <h3
      class="mt-2 text-center text-lg font-semibold text-rose-600 dark:text-rose-400"
    >
      {{ product.description }}
    </h3>
  </a>
</template>
