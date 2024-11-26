<template>
  <q-page>
    <PaymentMethodContent />
  </q-page>
</template>

<script>
import PaymentMethodContent from "src/components/PaymentPage/PaymentMethodContent.vue";

export default {
  name: "PaymentMethodPage",
  components: {
    PaymentMethodContent,
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
