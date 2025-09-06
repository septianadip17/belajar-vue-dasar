<template>
  <div class="container">
    <!-- Counter -->
    <h2>Counter</h2>
    <p>Angka: {{ count }}</p>
    <button @click="count++">Tambah</button>
    <button @click="count--">Kurang</button>
    <hr />

    <!-- Form User -->
    <h2>Form User</h2>
    <form @submit.prevent="submitForm">
      <input v-model="user.name" placeholder="Nama" />
      <input v-model="user.age" type="number" placeholder="Umur" />
      <button type="submit">Simpan</button>
    </form>

    <p>Output:</p>
    <p>Nama: {{ user.name }}</p>
    <p>Umur: {{ user.age }}</p>
  </div>
</template>

<script setup>
import { ref, reactive } from "vue"

// Counter pakai ref
const count = ref(0)

// User pakai reactive
const user = reactive({
  name: "",
  age: null,
})

const submitForm = () => {
  alert(`Nama: ${user.name}, Umur: ${user.age}`)
}
</script>

<style>
.container {
  font-family: sans-serif;
  padding: 20px;
}

button {
  margin: 5px;
}
</style>