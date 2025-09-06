<script setup>
import { ref } from "vue"

const count = ref(0)

const increment = () => {
  count.value++
}
</script>

<template>
  <div>
    <h1>Count: {{ count }}</h1>
    <button @click="increment">Tambah</button>
  </div>
</template>