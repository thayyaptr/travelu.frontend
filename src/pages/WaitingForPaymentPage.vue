<template>
  <q-page>
    <WaitingForPaymentContent />
  </q-page>
</template>

<script>
import WaitingForPaymentContent from "src/components/PaymentPage/WaitingForPaymentContent.vue";

export default {
  name: "WaitingForPaymentPage",
  components: {
    WaitingForPaymentContent,
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
