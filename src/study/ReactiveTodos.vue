<script setup>
import { reactive } from "vue"

const todos = reactive(["Belajar Vue", "Belajar React"])

const addTodo = () => {
  todos.push("Belajar Pinia")
}
</script>

<template>
  <div>
    <h3>Daftar Todo:</h3>
    <ul>
      <li v-for="(todo, index) in todos" :key="index">{{ todo }}</li>
    </ul>
    <button @click="addTodo">Tambah Todo</button>
  </div>
</template>