<template>
  <q-page>
    <LoginContent />
  </q-page>
</template>

<script>
import LoginContent from "../components/LoginPage/LoginContent.vue";

export default {
  name: "LoginPage",
  components: {
    LoginContent,
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
