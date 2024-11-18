<template>
  <div class="q-pa-md">
    <!-- Carousel -->
    <q-carousel v-model="slide" animated arrows navigation infinite>
      <q-carousel-slide
        v-for="slide in slides"
        :key="slide.name"
        :name="slide.name"
        :img-src="slide.imgSrc"
      />
    </q-carousel>

    <!-- "Click And Go" Section -->
    <div class="click-and-go">
      <h2>Click And Go !!!</h2>
      <div class="search-form">
        <select class="dropdown">
          <option>Select Departure</option>
        </select>
        <select class="dropdown">
          <option>Select Destination</option>
        </select>
        <select class="dropdown">
          <option>Passengers</option>
        </select>
        <input type="date" class="date-input" />
        <button class="search-button">Search</button>
      </div>
    </div>

    <!-- Footer Section -->
    <div class="footer-section">
      <div class="footer-content">
        <h3>Our Services</h3>
        <p>About Us</p>
        <p>Our Branches</p>
      </div>
      <div class="footer-content">
        <h3>Download The App</h3>
        <img src="assets/appstore.png" alt="App Store" class="app-store" />
        <img src="assets/googleplay.png" alt="Google Play" class="google-play" />
      </div>
      <div class="footer-content">
        <h3>Contact Us</h3>
        <p>Jl. Telkom II blok i-2 No.48, Bandung</p>
        <p>Phone: 022 30 500 800</p>
      </div>
    </div>
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
/* Carousel */
.q-carousel-slide img {
  object-fit: cover;
  height: 300px;
}

/* Click And Go Section */
.click-and-go {
  text-align: center;
  margin: 40px 0;
}

.click-and-go h2 {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 20px;
}

.search-form {
  display: flex;
  justify-content: center;
  gap: 10px;
  flex-wrap: wrap;
}

.dropdown {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.date-input {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.search-button {
  padding: 10px 20px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.search-button:hover {
  background-color: #0056b3;
}

/* Footer Section */
.footer-section {
  display: flex;
  justify-content: space-between;
  padding: 20px;
  background-color: #dbe9f6;
  margin-top: 40px;
}

.footer-content {
  flex: 1;
  margin: 0 10px;
}

.footer-content h3 {
  font-size: 18px;
  margin-bottom: 10px;
}

.footer-content p {
  font-size: 14px;
  margin: 5px 0;
}

.app-store,
.google-play {
  width: 120px;
  margin-top: 10px;
}
</style>
