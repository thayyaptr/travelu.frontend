<template>
  <q-page
    style="display: flex; justify-content: center; align-items: flex-start"
  >
    <OrderTicketContent style="width: 90%" />
  </q-page>
</template>

<script>
import OrderTicketContent from "src/components/OrderPage/OrderTicketContent.vue";

export default {
  name: "OrderTicketPage",
  components: {
    OrderTicketContent,
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
