<script setup>
import { ref } from "vue"

const categories = ref([
  { name: "Buah", items: ["Apel", "Mangga", "Jeruk"] },
  { name: "Sayur", items: ["Bayam", "Wortel", "Tomat"] }
])
</script>

<template>
  <div v-for="category in categories" :key="category.name">
    <h4>{{ category.name }}</h4>
    <ul>
      <li v-for="item in category.items" :key="item">{{ item }}</li>
    </ul>
  </div>
</template>