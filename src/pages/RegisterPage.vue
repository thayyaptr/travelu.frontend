<template>
  <q-page>
    <RegisterContent />
  </q-page>
</template>

<script>
import RegisterContent from "src/components/RegisterPage/RegisterContent.vue";
import LoginContent from "../components/LoginPage/LoginContent.vue";

export default {
  name: "RegisterPage",
  components: {
    RegisterContent,
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
