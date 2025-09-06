<script setup>
import HelloWorld from './components/HelloWorld.vue'
const isLoggedIn = true
const users = ["Budi", "Siti", "Andi"]
const message = "Hello Vue"
import { ref } from "vue"

const count = ref(0)

const increment = () => {
  count.value++
}
</script>

<template>
  <!-- v-if -->
  <p v-if="isLoggedIn">Selamat datang!</p>
  <p v-else>Silakan login</p>

  <!-- v-for -->
  <ul>
    <li v-for="(user, index) in users" :key="index">{{ user }}</li>
  </ul>

  <!-- v-model -->
  <input v-model="message" />
  <p>Pesan: {{ message }}</p>
  <HelloWorld name="Budi" age="30" isAdmin />

  <!-- ref -->
  <div>
    <h1>Count: {{ count }}</h1>
    <button @click="increment">Tambah</button>
  </div>

  
</template>