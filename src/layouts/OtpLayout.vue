<template>
  <q-layout view="lHh Lpr lFf">
    <!-- Page Navbar -->
    <OtpNavbar />

    <!-- Page Body -->
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import OtpNavbar from "src/components/OtpNavbar.vue";

// Define component options
defineOptions({
  name: "OtpLayout",
});
</script>

<style scoped>
/* Add styles specific to MainLayout here if needed */
</style>
