<template>
  <q-layout view="lHh Lpr lFf">
    <!-- Page Navbar -->
    <PassNavbar />

    <!-- Page Body -->
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import PassNavbar from "src/components/PassNavbar.vue";

// Define component options
defineOptions({
  name: "MainLayout",
});
</script>

<style scoped>
/* Add styles specific to MainLayout here if needed */
</style>
