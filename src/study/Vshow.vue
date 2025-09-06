<script setup>
import { ref } from "vue"

const isVisible = ref(true)
</script>

<template>
  <div>
    <p v-show="isVisible">Teks ini bisa disembunyikan dengan v-show</p>
    <button @click="isVisible = !isVisible">Toggle</button>
  </div>
</template>