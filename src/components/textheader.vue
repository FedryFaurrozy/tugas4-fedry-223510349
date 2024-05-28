<template>
  <h1>
    {{ title || "tidak ada pesan" }}
  </h1>
</template>
<script setup>
defineProps({
  title: String,
});
</script>
