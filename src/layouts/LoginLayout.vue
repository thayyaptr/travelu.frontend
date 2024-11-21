<template>
  <q-layout view="lHh Lpr lFf">
    <!-- Page Navbar -->
    <LoginNavbar />

    <!-- Page Body -->
    <q-page-container>
      <router-view />
    </q-page-container>

    <!-- Page Footer -->
    <footer>
      <!-- Add your footer content here -->
      <PageFooter />
    </footer>
  </q-layout>
</template>

<script setup>
import LoginNavbar from "src/components/LoginNavbar.vue"; // Ensure the path is correct
import PageFooter from "src/components/PageFooter.vue"; // Ensure the path is correct

// Define component options
defineOptions({
  name: "MainLayout",
});
</script>

<style scoped>
/* Add styles specific to MainLayout here if needed */
</style>
