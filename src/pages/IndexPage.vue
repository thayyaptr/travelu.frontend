<template>
  <q-page>
    <BannerHome />
    <ClickAndGo />
  </q-page>
</template>

<script>
import BannerHome from "../components/IndexPage/BannerHome.vue";
import ClickAndGo from "../components/IndexPage/ClickAndGo.vue";

export default {
  name: "IndexPage",
  components: {
    BannerHome,
    ClickAndGo,
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
