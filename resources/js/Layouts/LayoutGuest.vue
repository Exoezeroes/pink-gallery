<script setup>
import { useStyleStore } from "@/Stores/style.js";
import menuNavBar from "@/menuNavBar";
import AppIcon from "@/Components/AppIcon.vue";
import NavBar from "@/Components/NavBar.vue";

const layoutAsidePadding = "xl:pl-60";

const styleStore = useStyleStore();

const menuClick = (event, item) => {
  if (item.isToggleLightDark) {
    styleStore.setDarkMode();
  }
};
</script>

<template>
  <div :class="{ dark: styleStore.darkMode }">
    <div
      class="min-h-screen w-screen bg-gray-50 transition-position dark:bg-slate-800 dark:text-slate-100 lg:w-auto"
    >
      <NavBar :menu="menuNavBar" @menu-click="menuClick">
        <AppIcon />
      </NavBar>
      <slot />
    </div>
  </div>
</template>
