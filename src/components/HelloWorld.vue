<script setup>
defineProps({
  name: String,
  age: Number,
  isAdmin: Boolean
})
</script>

<template>
  <h2>Halo, {{ name }}!</h2>

  <p v-if="age">Umur: {{ age }} tahun</p>
  <p v-else>Umur tidak diketahui</p>
  <p v-if="isAdmin">Admin</p>
  <p v-else>Bukan Admin</p>
</template>