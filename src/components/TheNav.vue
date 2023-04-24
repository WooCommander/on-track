<script setup>
import NavItem from "./NavItem.vue"
import { ClockIcon, ListBulletIcon, ChartBarIcon } from "@heroicons/vue/24/outline";
const navItems = [{ name: "timeline", component: ClockIcon }, { name: "activites", component: ListBulletIcon }, { name: "progress", component: ChartBarIcon }]

</script>
<template>
  <nav class="sticky bottom-0 z-10 bg-white">
    <ul class="flex items-center justify-around border-t">
      <NavItem v-for="page in navItems" :href="'#' +
        page.name">
        <component :is="page.component" class="h-6 w-6" /> {{ page.name }}
      </NavItem>

    </ul>
  </nav>
</template>