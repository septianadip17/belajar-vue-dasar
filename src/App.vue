<script setup>
import { reactive } from "vue"

const user = reactive({
  name: "Budi",
  age: 20
})

const tambahUmur = () => {
  user.age++
}
</script>

<template>
  <div>
    <p>Nama: {{ user.name }}</p>
    <p>Umur: {{ user.age }}</p>
    <button @click="tambahUmur">Tambah Umur</button>
  </div>
</template>