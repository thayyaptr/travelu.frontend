<template>
  <q-header elevated>
    <q-toolbar style="background-color: #e2efff; height: 8vh">
      <q-toolbar-title>
        <q-col>
          <router-link to="/">
            <img src="path/to/logo.png" alt="Logo" style="height: 40px" />
          </router-link>
        </q-col>
      </q-toolbar-title>

      <q-space />

      <q-col style="text-align: center; color: black">
        <h5>asdfasd</h5>
      </q-col>
      <q-col style="text-align: center; color: black">
        <h5>asdfasd</h5>
      </q-col>
      <q-col style="text-align: center; color: black">
        <h5>asdfasd</h5>
      </q-col>

      <q-space />

      <q-col style="display: flex; align-items: center; color: black">
        <img
          src="path/to/user-pic.png"
          alt="User  Pic"
          class="q-mr-sm"
          style="height: 40px; border-radius: 50%"
        />
        <span class="q-mr-sm"
          ><h6>{{ username }}</h6></span
        >
        <q-btn flat icon="menu" @click="toggleMenu" />
      </q-col>
    </q-toolbar>
  </q-header>
</template>

<script>
export default {
  data() {
    return {
      username: "Hanif",
    };
  },
  methods: {
    toggleMenu() {
      // Logic to toggle the user profile menu
      console.log("Menu toggled");
    },
  },
};
</script>

<style scoped>
.q-header {
  background-color: #f8f9fa; /* Adjust the background color */
}

.custom-toolbar {
  background-color: #e2efff; /* Set the toolbar color */
}
</style>
