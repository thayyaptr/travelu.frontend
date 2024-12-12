<template>
  <q-header elevated>
    <q-toolbar
      style="background-color: #0077b6; color: white; font-size: 2rem"
      class="q-pa-sm"
    >
      <a href="/">
        <img :src="logo" style="max-height: 7vh" />
      </a>
      <span style="font-weight: bold" class="q-mr-lg">Travel-U</span>
    </q-toolbar>
  </q-header>
</template>

<script>
export default {
  data() {
    return {
      username: "Hanif",
      logo: "/logo-text.png",
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
