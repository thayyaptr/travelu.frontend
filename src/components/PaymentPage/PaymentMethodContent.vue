<template>
    <div class="row" style= "height: 5vh; font-size: 2rem; padding : 30px 40px 10px 40px;  border-bottom: 2px solid black; padding-bottom: 120px; margin-bottom: 10px; margin-left : 70px ;margin-right : 70px;">
        <div class="col-7 text-align text-black align-self-center">
            Bandung, Buah Batu -> Jakarta, Grogol <br>
            Monday, 28 October 2024 | 1 Passenger
        </div>
        
        <div class="col-5" style="display: flex; justify-content: flex-end; position: relative;">
            <br>
            <div class="dropdown-container">
            <button class="dropdown-btn" @click="toggleDropdown">
                Order Details
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
/* Kontainer dropdown */
.dropdown-container {
  position: relative; /* Membuat menu dropdown terikat dengan tombol */
}

/* Tombol dropdown */
.dropdown-btn {
  background-color: #a3b8d8;
  color: white;
  border: none;
  padding: 10px 20px;
  font-size: 16px;
  font-weight: bold;
  border-radius: 50px; /* Membuat tombol berbentuk oval */
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 8px; /* Jarak antara teks dan panah */
}

/* Hover efek untuk tombol */
.dropdown-btn:hover {
  background-color: #91a8cc;
}

/* Panah di sebelah kanan tombol */
.dropdown-arrow {
  width: 0;
  height: 0;
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: 5px solid white;
}

/* Menu dropdown */
.dropdown-menu {
  position: absolute;
  top: 100%; /* Muncul tepat di bawah tombol */
  right: 0; /* Muncul di sisi kanan tombol */
  background-color: white;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  list-style: none;
  margin: 5px 0 0;
  padding: 0;
  min-width: 200px; /* Lebar minimum dropdown */
  z-index: 1000;
}

/* Item dropdown */
.dropdown-item {
  padding: 10px 15px;
  cursor: pointer;
  font-size: 14px;
  color: #333;
}

/* Hover efek untuk item dropdown */
.dropdown-item:hover {
  background-color: #f5f5f5;
}
</style>
