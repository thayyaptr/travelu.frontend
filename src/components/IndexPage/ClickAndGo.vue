<template>
  <div class="cover">
    <div style="max-width: 1400px; width: 90%; margin: 0 auto">
      <h2 class="q-mx-md">Click and Go!</h2>
      <div class="row">
        <div
          class="col-12 row q-mx-md"
          style="
            background-color: #dbe9f6;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
          "
        >
          <q-select
            v-model="departure"
            :options="departureOptions"
            label="Pilih Keberangkatan"
            class="col-5 q-pa-md"
          />
          <div class="col-2"></div>
          <q-select
            v-model="destination"
            :options="destinationOptions"
            label="Pilih Destinasi"
            class="col-5 q-pa-md"
          />
          <q-select
            v-model="passengerCount"
            :options="passengerOptions"
            label="Jumlah Penumpang"
            class="col-3 q-pa-md"
          />

          <!-- Template buat Date Picker dari Quasar -->
          <!-- https://quasar.dev/vue-components/date#custom-title-and-subtitle -->
          <q-input
            class="col-3 q-pa-md"
            filled
            v-model="date"
            mask="date"
            :rules="['date']"
          >
            <template v-slot:append>
              <q-icon name="event" class="cursor-pointer">
                <q-popup-proxy
                  cover
                  transition-show="scale"
                  transition-hide="scale"
                >
                  <q-date v-model="date">
                    <div class="row items-center justify-end">
                      <q-btn v-close-popup label="Close" color="primary" flat />
                    </div>
                  </q-date>
                </q-popup-proxy>
              </q-icon>
            </template>
          </q-input>
          <div class="col-2"></div>
          <div
            class="col-2 q-pa-md"
            style="
              background-color: #dbe9f6;
              border-radius: 8px;
              text-align: center;
            "
          >
            <q-btn
              label="Search"
              icon="search"
              @click="onSearch"
              color="primary"
              padding="md"
            />
          </div>
          <div class="col-2"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      departure: null,
      destination: null,
      passengerCount: null,
      schedule: null,
      departureOptions: ["Option 1", "Option 2", "Option 3"],
      destinationOptions: ["Destination 1", "Destination 2", "Destination 3"],
      passengerOptions: [1, 2, 3, 4, 5],
    };
  },
  methods: {
    onSearch() {
      // Handle search logic here
      console.log("Searching for:", {
        departure: this.departure,
        destination: this.destination,
        passengerCount: this.passengerCount,
        schedule: this.schedule,
      });
    },
  },
};
</script>

<style scoped>
.cover {
  background-image: url("https://www.mylintas.co.id/assets/images/beranda/bg-reservasi.png");
  background-size: cover;
  width: 100%;
  padding: 20px 0;
}
</style>
