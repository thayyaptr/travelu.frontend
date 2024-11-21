<template>
  <q-header elevated>
    <q-toolbar
      style="background-color: #e2efff; color: black; font-size: 2.25rem"
      class="q-pa-md"
    >
      <q-avatar size="5rem">
        <img :src="logo" />
      </q-avatar>
      <span style="font-weight: bold" class="q-mr-lg">Travel-U</span>
      <div>
        <q-btn
          flat
          size="1.5rem"
          style="font-weight: 500"
          label="Beranda"
          @click="goHome"
        />
        <q-btn
          flat
          size="1.5rem"
          style="font-weight: 500"
          label="Pesan Tiket"
          @click="goHome"
        />
        <q-btn
          flat
          size="1.5rem"
          style="font-weight: 500"
          label="Komplain"
          @click="goHome"
        />
        <q-btn
          flat
          size="1.5rem"
          style="font-weight: 500"
          label="Tentang Kami"
          @click="goHome"
        />
      </div>
      <q-toolbar-title> </q-toolbar-title>

      <q-col style="display: flex; align-items: center">
        <img
          src="https://static.vecteezy.com/system/resources/previews/036/594/092/non_2x/man-empty-avatar-photo-placeholder-for-social-networks-resumes-forums-and-dating-sites-male-and-female-no-photo-images-for-unfilled-user-profile-free-vector.jpg"
          alt="User  Pic"
          class="q-mr-lg"
          style="height: 4rem; border-radius: 50%"
        />
        <span class="q-mr-sm" style="font-size: 1.5rem; font-weight: bold">{{
          username
        }}</span>
        <q-btn
          flat
          icon="menu"
          size="1.75rem"
          @click="toggleMenu"
          aria-label="Toggle Menu"
        />
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
