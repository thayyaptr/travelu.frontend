<template>
  <q-header elevated>
    <q-toolbar style="background-color: #e2efff; height: 10vh">
      <q-toolbar-title>
        <q-col style="display: flex; align-items: center">
          <router-link to="/">
            <img
              :src="logo"
              alt="Logo"
              style="height: 7vh; margin-right: 16px"
            />
          </router-link>
          <q-btn
            flat
            label="Home"
            @click="goHome"
            class="q-mr-md"
            text-color="black"
          />
          <q-btn
            flat
            label="Book Tiket"
            @click="goToBookTicket"
            class="q-mr-md"
            text-color="black"
          />
          <q-btn
            flat
            label="Suggestion"
            @click="goToSuggestion"
            text-color="black"
          />
        </q-col>
      </q-toolbar-title>

      <q-space />

      <q-col style="display: flex; align-items: center; color: black">
        <img
          src="path/to/user-pic.png"
          alt="User  Pic"
          class="q-mr-sm"
          style="height: 40px; border-radius: 50%"
        />
        <span class="q-mr-sm">{{ username }}</span>
        <q-btn flat icon="menu" @click="toggleMenu" aria-label="Toggle Menu" />
      </q-col>
    </q-toolbar>
  </q-header>
</template>

<script>
export default {
  data() {
    return {
      username: "Hanif",
      logo: "/logo.png",
    };
  },
  methods: {
    goHome() {
      this.$router.push("/");
    },
    goToBookTicket() {
      this.$router.push("/book-ticket"); // Adjust the path as needed
    },
    goToSuggestion() {
      this.$router.push("/suggestion"); // Adjust the path as needed
    },
    toggleMenu() {
      // Implement your menu toggle logic here
    },
  },
};
</script>

<style scoped>
.q-header {
  background-color: black; /* Adjust the background color */
}

.custom-toolbar {
  background-color: black; /* Set the toolbar color */
}
</style>
