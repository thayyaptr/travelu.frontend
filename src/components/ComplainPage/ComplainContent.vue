<template>
  <q-page>
    <div class="main-content">
      <h1>Complain</h1>
      <p>Silakan masukkan keluhan Anda di bawah ini:</p>
      <textarea
        placeholder="Ketik keluhan Anda di sini..."
        class="feedback-textarea"
      ></textarea>
      <br />
      <button class="submit-button">Submit</button>
    </div>
  </q-page>
</template>

<script setup>
defineOptions({
  name: "ComplainContent", // Optional: define a name for this component
});
</script>

<style scoped>
.main-content {
  padding: 20px;
  text-align: center;
}

.feedback-textarea {
  width: 80%;
  height: 100px;
  margin: 10px 0;
  padding: 10px;
  font-size: 16px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.submit-button {
  padding: 10px 20px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.submit-button:hover {
  background-color: #0056b3;
}
</style>
