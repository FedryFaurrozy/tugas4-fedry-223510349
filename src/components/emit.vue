<template>
  <br />
  <button @click="ubahText">click me</button> <br />
  <br />
</template>
<script setup>
const emit = defineEmits(["response"]);
function ubahText() {
  emit("response", "hello ini data yang berada pada page anak sebagai emmit");
}
</script>
