<script setup>
defineProps({
  text: String,
});
</script>

<template>
  <Transition
    appear
    enter-from-class="opacity-0 scale-0"
    enter-to-class="opacity-100 scale-100"
    enter-active-class="transition duration-700"
  >
    <h1
      class="rounded-lg bg-gray-50/75 p-8 text-9xl shadow dark:bg-slate-900/50 lg:text-[10rem]"
    >
      <span class="text-outline">
        {{ text }}
      </span>
    </h1>
  </Transition>
</template>

<style>
.text-outline {
  color: white; /* Unfortunately you can't use transparent here … */
  text-shadow: -1px -1px 0 #f472b6, 1px -1px 0 #f472b6, -1px 1px 0 #f472b6,
    1px 1px 0 #f472b6;
}

@supports ((text-stroke: 4px #f472b6) or (-webkit-text-stroke: 4px #f472b6)) {
  .text-outline {
    color: transparent;
    -webkit-text-stroke: 4px #f472b6;
    text-shadow: none;
  }
}
</style>
