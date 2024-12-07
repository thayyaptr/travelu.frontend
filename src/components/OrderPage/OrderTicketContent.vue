<template>
  <div class="q-pa-lg flex flex-center">
    <div class="col q-pt-lg" style="width: 90%">
      <!-- Informasi Utama -->
      <div class="row" style="font-size: 1.5rem">
        <div class="col-7 text-align text-black" style="font-weight: bold;">
          Bandung, Buah Batu -> Jakarta, Grogol <br />
          Monday, 28 October 2024 | 1 Passenger
        </div>

        <div
          class="col-5"
          style="display: flex; justify-content: flex-end; position: relative"
        >
          <br />
          <div class="dropdown-container">
            <button class="dropdown-btn" @click="toggleDropdown">
              Change Destination
              <span class="dropdown-arrow"></span>
            </button>
            <ul v-if="isOpen" class="dropdown-menu">
              <li class="dropdown-item">Option 1</li>
              <li class="dropdown-item">Option 2</li>
              <li class="dropdown-item">Option 3</li>
            </ul>
          </div>
        </div>
      </div>

      <hr style="border: 1px solid black; margin: 10px 0" />
      <!-- Select Departure Time -->
      <div
        class="row q-my-sm"
        style="background-color: #f0f0f9; font-size: 1.2rem"
      >
        <!-- Section 1 -->
        <div class="row q-my-sm" style="width: 100%; margin-left:15px; margin-right:15px">
            <div class="col-8" style="margin-left: 30px; margin-top: 10px;">
            <img src="https://cdn4.iconfinder.com/data/icons/delivery-shipping-4/32/delivery-25-512.png" alt="BCA Mobile Logo" style="height:2rem;width:2rem
                    ;">
                    <div class="value" style="font-weight: bold; margin-left:5px;" >Travel-U</div>
            <div class="value" style="font-size:0.9rem;">07.00  Pool Buah Batu</div><br>
            <div class="value" style="font-size:0.5rem;">3j 0m</div><br>
            <div class="value" style="font-size:0.9rem;">10.00  Pool Grogol</div>
            
          </div>
            <div class="col-2" style="margin-left: 30px; margin-top: 10px;">
            <br>
            <div class="value" style="font-size:0.9rem;">Rp 150.000/seat</div>
            <div class="value" style="font-size:0.9rem;">8 Capacity</div>
          </div>
        </div>

      </div>
        
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false, // Mengontrol buka/tutup dropdown
    };
  },
  methods: {
    toggleDropdown() {
      this.isOpen = !this.isOpen; // Membalik status dropdown
    },
  },
};
</script>

<style scoped>
/* Gaya untuk container rounded rectangle */
.row.q-my-sm {
  border-radius: 15px; /* Membuat sudut membulat */
  overflow: hidden; /* Opsional, untuk memastikan isi container tetap rapi */
}

/* Gaya untuk label */
.span {
  color: #555; /* Warna abu-abu untuk label */
  font-size: 0.9rem; /* Ukuran font lebih kecil untuk label */
  font-weight: normal; /* Berat font normal */
}

/* Gaya untuk value */
.value {
  color: #333; /* Warna lebih gelap untuk value */
  font-size: 1.2rem; /* Ukuran font lebih besar untuk value */
  font-weight: bold; /* Berat font bold */
}

/* Tombol Dropdown */
.dropdown-container {
  position: relative;
}
.dropdown-btn {
  background-color: #a3b8d8;
  color: white;
  border: none;
  padding: 10px 20px;
  font-size: 16px;
  font-weight: bold;
  border-radius: 50px;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 8px;
}
.dropdown-btn:hover {
  background-color: #91a8cc;
}
.dropdown-arrow {
  width: 0;
  height: 0;
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: 5px solid white;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  right: 0;
  background-color: white;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  list-style: none;
  margin: 5px 0 0;
  padding: 0;
  min-width: 200px;
  z-index: 1000;
}
.dropdown-item {
  padding: 10px 15px;
  cursor: pointer;
  font-size: 14px;
  color: #333;
}
.dropdown-item:hover {
  background-color: #f5f5f5;
}

</style>
