<script setup>
import { ref } from "vue"

const users = ref([
  { id: 1, name: "Budi", age: 20 },
  { id: 2, name: "Siti", age: 22 },
  { id: 3, name: "Andi", age: 25 }
])
</script>

<template>
  <div v-for="user in users" :key="user.id" class="card">
    <h3>{{ user.name }}</h3>
    <p>Umur: {{ user.age }}</p>
  </div>
</template>