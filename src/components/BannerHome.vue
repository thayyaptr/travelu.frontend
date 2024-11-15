<template>
  <div class="q-pa-md">
    <q-carousel v-model="slide" animated arrows navigation infinite>
      <q-carousel-slide
        v-for="slide in slides"
        :key="slide.name"
        :name="slide.name"
        :img-src="slide.imgSrc"
      />
    </q-carousel>
  </div>
</template>

<script setup>
import { ref } from "vue";

// Define the reactive state for the current slide
const slide = ref(1);

// Define an array of slides for better maintainability
const slides = [
  { name: 1, imgSrc: "https://cdn.quasar.dev/img/mountains.jpg" },
  { name: 2, imgSrc: "https://cdn.quasar.dev/img/parallax1.jpg" },
  { name: 3, imgSrc: "https://cdn.quasar.dev/img/parallax2.jpg" },
  { name: 4, imgSrc: "https://cdn.quasar.dev/img/quasar.jpg" },
];
</script>

<style scoped>
/* Add styles specific to BannerHome here if needed */
</style>
