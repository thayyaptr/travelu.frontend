<template>
  <q-page>
    <PaymentStatusFailedContent />
  </q-page>
</template>

<script>
import PaymentStatusFailedContent from "src/components/PaymentPage/PaymentStatusFailedContent.vue";

export default {
  name: "PaymentStatusFailedPage",
  components: {
    PaymentStatusFailedContent,
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
