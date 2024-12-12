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
      <div>
        <q-btn
          flat
          size="1.3rem"
          style="font-weight: 400"
          label="Beranda"
          @click="goHome"
        />
        <q-btn
          flat
          size="1.3rem"
          style="font-weight: 400"
          label="Pesan Tiket"
          @click="goHome"
        />
        <a href="/complain" style="color: white">
          <q-btn flat size="1.3rem" style="font-weight: 400" label="Komplain" />
        </a>

        <q-btn
          flat
          size="1.3rem"
          style="font-weight: 400"
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
        >
          <q-menu transition-show="jump-down" transition-hide="jump-up">
            <q-list style="min-width: 100px">
              <q-item @click="goToLogin" clickable>
                <q-item-section>Login</q-item-section>
              </q-item>
              <q-item @click="goToRegister" clickable>
                <q-item-section>Register</q-item-section>
              </q-item>
            </q-list>
          </q-menu>
        </q-btn>
      </q-col>
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
    goToComplain() {
      this.$router.push("/complain"); // Adjust the path as needed
    },
    goToLogin() {
      this.$router.push("/login");
    },
    goToRegister() {
      this.$router.push("/register");
    },
    toggleMenu() {
      this.menu = !this.menu; // Toggle menu state
    },
  },
};
</script>

<style scoped>
.q-header {
  background-color: rgb(255, 255, 255); /* Adjust the background color */
}

.custom-toolbar {
  background-color: rgb(255, 255, 255); /* Set the toolbar color */
}
</style>
