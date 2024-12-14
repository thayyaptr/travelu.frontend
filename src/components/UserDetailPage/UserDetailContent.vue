<template>
  <div style="background-color: #E2EFFF; font-size: 1.2rem; padding: 1rem;">
    <!-- First Row -->
    <div class="row" style="background-color: #FFFFFF; padding: 1rem; margin-bottom: 1rem; display: flex; justify-content: space-between; align-items: center;">
      <div class="col" style="text-align: left;">
        <div class="value" style="font-size: 2.5rem;">Hai, Ayman Shafwan!</div>
        <div class="span" style="font-weight: bold;">Email: ayman40@gmail.com</div>
        <div class="span" style="font-weight: bold;">Phone Number: +62 812-487-860</div>
      </div>
      <div class="col" style="text-align: right;">
        <img src="https://tse3.mm.bing.net/th?id=OIP.rretLuneJE9smMh1q3rBdgHaHa&pid=Api&P=0&h=220" alt="Identity Logo" style="height:9rem; width:9rem;">
      </div>
    </div>

    <!-- Second Row -->
    <div class="row" style="background-color: #FFFFFF; padding: 1rem; box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);">
      <form style="width: 100%;">
        <div style="margin-bottom: 15px;">
          <label for="fullName" class="span">Full Name:</label>
          <input type="text" id="fullName" name="fullName" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 5px;">
        </div>
        <div style="margin-bottom: 15px;">
          <label for="fullAddress" class="span">Full Address:</label>
          <input type="text" id="fullAddress" name="fullAddress" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 5px;">
        </div>
        <div style="margin-bottom: 15px;">
          <label for="phoneNumber" class="span">Phone Number:</label>
          <input type="tel" id="phoneNumber" name="phoneNumber" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 5px;">
        </div>
        <div style="margin-bottom: 15px;">
          <label for="email" class="span">Email:</label>
          <input type="email" id="email" name="email" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 5px;">
        </div>
        <div style="margin-bottom: 15px;">
          <label for="password" class="span">Password:</label>
          <input type="password" id="password" name="password" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 5px;">
        </div>
        <div style="text-align: right;">
          <button type="submit" style="background-color: #007BFF; color: #FFF; padding: 10px 20px; border: none; border-radius: 5px; cursor: pointer;">Submit</button>
        </div>
      </form>
    </div>
  </div>
</template>

<style scoped>
/* Gaya untuk container rounded rectangle */

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

/* Gaya untuk input dan tombol */
input {
  font-size: 1rem;
  margin-top: 5px;
  margin-bottom: 5px;
}

button:hover {
  background-color: #0056b3;
}
</style>


