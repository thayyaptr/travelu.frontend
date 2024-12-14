<template>
  <q-page>
    <BannerHome />
    <ClickAndGo :KotaList="KotaList" :CabangList="CabangList" />
    <DestinasiWisata />
  </q-page>
</template>

<script>
import BannerHome from "../components/IndexPage/BannerHome.vue";
import ClickAndGo from "../components/IndexPage/ClickAndGo.vue";
import DestinasiWisata from "../components/IndexPage/DestinasiWisata.vue";
import { ref, onMounted } from "vue";
import { api } from "boot/axios";

export default {
  name: "IndexPage",
  components: {
    BannerHome,
    ClickAndGo,
    DestinasiWisata,
  },
  setup() {
    const loadedKota = ref(false);
    const loadedCabang = ref(false);
    const KotaList = ref([]);
    const CabangList = ref([]);

    function loadKota() {
      api
        .get("/kotas")
        .then((response) => {
          KotaList.value = response.data;
          loadedKota.value = true; // Corrected variable name
        })
        .catch((error) => {
          console.error("Error fetching Kota list:", error); // Error handling
        });
    }
    function loadCabang() {
      api
        .get("/cabangs")
        .then((response) => {
          CabangList.value = response.data;
          loadedCabang.value = true; // Corrected variable name
        })
        .catch((error) => {
          console.error("Error fetching Cabang list:", error); // Error handling
        });
    }

    onMounted(() => {
      // loadKota();
      // loadCabang();
    });

    return {
      loadedKota,
      loadedCabang,
      KotaList,
      CabangList,
    };
  },
};
</script>

<style scoped>
/* Add styles specific to IndexPage here if needed */
</style>
