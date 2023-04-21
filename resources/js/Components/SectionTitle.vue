<script setup>
defineProps({
  custom: Boolean,
  first: Boolean,
  last: Boolean,
});
</script>

<template>
  <section class="px-6 py-24 text-center lg:mx-auto lg:max-w-2xl lg:px-0">
    <slot />
  </section>
</template>
