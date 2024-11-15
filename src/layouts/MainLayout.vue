<template>
  <q-layout view="lHh Lpr lFf">
    <!-- Page Navbar -->
    <PageNavbar />

    <!-- Page Body -->
    <q-page-container>
      <router-view />
    </q-page-container>

    <!-- Page Footer -->
    <footer>
      <!-- Add your footer content here -->
    </footer>
  </q-layout>
</template>

<script setup>
import PageNavbar from "src/components/PageNavbar.vue"; // Ensure the path is correct

// Define component options
defineOptions({
  name: "MainLayout",
});
</script>

<style scoped>
/* Add styles specific to MainLayout here if needed */
</style>
