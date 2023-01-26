<script setup lang="ts">
import { ref } from "vue";
import TopNav from "@/components/TopNav.vue";
import LeftNav from "@/components/LeftNav.vue";
</script>

<template>
  <TopNav />
  <main>
    <LeftNav />
    <div>Main View</div>
  </main>
</template>

<style scoped>
main {
  width: 100%;
  height: 100%;
  display: flex;
}
</style>
