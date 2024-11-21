<template>
  <q-header elevated>
    <q-toolbar
      style="background-color: #e2efff; color: black; font-size: 2.25rem"
      class="q-pa-sm"
    >
      <q-avatar size="5rem">
        <img :src="logo" />
      </q-avatar>
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
