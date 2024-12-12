<template>
  <q-page>
    <UserDetailContent />
  </q-page>
</template>

<script>
import UserDetailContent from "src/components/UserDetailPage/UserDetailContent.vue";

export default {
  name: "UserDetailPage",
  components: {
    UserDetailContent,
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
