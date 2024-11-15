<template>
  <q-header elevated>
    <q-toolbar style="background-color: #e2efff; height: 8vh">
      <q-toolbar-title>
        <q-col>
          <router-link to="/">
            <img :src="logo" alt="Logo" style="height: 40px" />
          </router-link>
        </q-col>
      </q-toolbar-title>

      <q-space />

      <q-col class="q-px-md" style="text-align: left; color: black">
        <h5>Home</h5>
      </q-col>
      <q-col class="q-px-md" style="text-align: left; color: black">
        <h5>Book Tiket</h5>
      </q-col>
      <q-col class="q-px-md" style="text-align: left; color: black">
        <h5>Suggestion</h5>
      </q-col>
      <q-space />

      <q-col style="display: flex; align-items: center; color: black">
        <img
          src="path/to/user-pic.png"
          alt="User  Pic"
          class="q-mr-sm"
          style="height: 40px; border-radius: 50%"
        />
        <span class="q-mr-sm">{{ username }}]]</span>
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
      logo: "/logo.jpg",
    };
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
