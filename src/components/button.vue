<template>
  <div class="button-container">
    <h3>Ini dari component Button sebagai pengatur warna tema</h3>
    <button class="submit" @click="setLightTheme">terang</button>
    <button class="cancel" @click="setDarkTheme">gelap</button>

    <TextCom />
  </div>
</template>

<script setup>
import TextCom from "./text.vue";
import { ref } from "vue";

const theme = ref("light");

function setLightTheme() {
  theme.value = "light";
  document.body.style.backgroundColor = "#FFFFFF"; // Warna putih
}

function setDarkTheme() {
  theme.value = "dark";
  document.body.style.backgroundColor = "#000000"; // Warna hitam
}
</script>
<style scoped>
.button-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
}

button {
  margin: 10px;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.submit {
  background-color: #ffffff; /* Warna putih */
  color: black;
}

.submit:hover {
  background-color: #e0e0e0; /* Warna putih lebih gelap */
}

.cancel {
  background-color: #000000; /* Warna hitam */
  color: white;
}

.cancel:hover {
  background-color: #404040; /* Warna hitam lebih terang */
}
</style>
