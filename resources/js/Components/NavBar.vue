<script setup>
import { ref } from "vue";
import { mdiClose, mdiDotsVertical } from "@mdi/js";
import { containerMaxW } from "@/config.js";
import BaseIcon from "@/Components/BaseIcon.vue";
import NavBarMenuList from "@/Components/NavBarMenuList.vue";
import NavBarItemPlain from "@/Components/NavBarItemPlain.vue";

defineProps({
  menu: {
    type: Array,
    required: true,
  },
});

const emit = defineEmits(["menu-click"]);

const menuClick = (event, item) => {
  emit("menu-click", event, item);
};

const isMenuNavBarActive = ref(false);
</script>

<template>
  <nav
    class="fixed inset-x-0 top-0 z-30 h-20 w-screen bg-gray-50/75 shadow-sm shadow-slate-400 transition-position dark:bg-slate-900/90 dark:shadow-pink-900/50 lg:w-auto"
  >
    <div class="flex lg:items-stretch" :class="containerMaxW">
      <div class="flex h-20 flex-1 items-stretch">
        <slot />
      </div>
      <div class="flex h-20 flex-none items-stretch lg:hidden">
        <NavBarItemPlain
          @click.prevent="isMenuNavBarActive = !isMenuNavBarActive"
        >
          <BaseIcon
            :path="isMenuNavBarActive ? mdiClose : mdiDotsVertical"
            size="24"
          />
        </NavBarItemPlain>
      </div>
      <div
        class="absolute left-0 top-20 max-h-screen-menu w-screen overflow-y-auto shadow-lg lg:static lg:flex lg:w-auto lg:overflow-visible lg:shadow-none"
        :class="[isMenuNavBarActive ? 'block' : 'hidden']"
      >
        <NavBarMenuList :menu="menu" @menu-click="menuClick" />
      </div>
    </div>
  </nav>
</template>
