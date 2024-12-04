<template>
  <q-page>
    <PaymentStatusSuccessContent />
  </q-page>
</template>

<script>
import PaymentStatusSuccessContent from "src/components/PaymentPage/PaymentStatusSuccessContent.vue";

export default {
  name: "PaymentStatusSuccessPage",
  components: {
    PaymentStatusSuccessContent,
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
