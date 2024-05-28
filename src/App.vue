<template>
  <div class="app-container">
    <h1>Selamat Datang</h1>
    <p>WEB MASIH TAHAP PENGEMBANGAN</p>
    <ButtonC />
  </div>
  <div class="response-container">
    <h2>Respon dari Komponen Anak:</h2>
    <p>{{ childMsg }}</p>
    <emitCom @response="ubahText" />
  </div>
  <slotCom />
</template>
<script setup>
import { ref } from "vue";
import EmitCom from "@/components/emit.vue";
const childMsg = ref("Tidak ada pesan");

function ubahText(msg) {
  childMsg.value = msg;
  console.log("Pesan yang diterima dari child: " + msg);
}
import ButtonC from "@/components/button.vue";
import slotCom from "@/components/slot.vue";
</script>
<style scoped>
.app-container {
  text-align: center;
  margin-top: 50px;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 8px;
}

.response-container {
  text-align: left;
  margin-top: 20px;
  padding: 20px;
  background-color: #ffffff;
  border: 1px solid #ccc;
  border-radius: 8px;
}

h1,
h2 {
  color: #333;
}

p {
  color: #666;
}
</style>
