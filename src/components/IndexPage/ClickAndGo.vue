<template>
  <div class="cover">
    <div style="max-width: 1140px; width: 90%; margin: 0 auto">
      <h2 class="q-mx-md">Click and Go!</h2>
      <div class="row">
        <div
          class="col-9 row q-mx-md"
          style="background-color: #dbe9f6; border-radius: 8px"
        >
          <q-select
            v-model="departure"
            :options="departureOptions"
            label="Pilih Keberangkatan"
            class="col-6 q-pa-md"
          />
          <q-select
            v-model="destination"
            :options="destinationOptions"
            label="Pilih Destinasi"
            class="col-6 q-pa-md"
          />
          <q-select
            v-model="passengerCount"
            :options="passengerOptions"
            label="Jumlah Penumpang"
            class="col-6 q-pa-md"
          />
          <q-input
            class="col-6 q-pa-md"
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
        </div>
        <div
          class="col-2 q-mx-lg"
          style="background-color: #dbe9f6; border-radius: 8px"
        >
          <q-btn
            label="Search"
            icon="search"
            class="search-button"
            @click="onSearch"
            color="primary"
            padding="lg"
            style="height: 100%"
          />
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

.dropdown {
  padding: 10px 0;
}

.search-button {
  width: 100%;
}
</style>
