<template>
  <q-page>
    <PaymentSuccessfulContent />
  </q-page>
</template>

<script>
import PaymentSuccessfulContent from "src/components/PaymentPage/PaymentSuccessfulContent.vue";

export default {
  name: "PaymentSuccessfulPage",
  components: {
    PaymentSuccessfulContent,
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
