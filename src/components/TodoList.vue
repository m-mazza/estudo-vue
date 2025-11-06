<script setup>
import { ref } from 'vue';

// Estado reativo: uma lista de tarefas
const todos = ref([
  { id: 1, text: 'Aprender Vue Composition API', done: false },
  { id: 2, text: 'Fazer o almoço', done: false },
  { id: 3, text: 'Responder e-mails', done: false }
]);

function toggleDone(todo) {
  todo.done = !todo.done;
}
</script>

<template>
  <div class="todo-list-container">
    <h2>Tarefas Pendentes</h2>
    <ul>
      <li v-for="todo in todos" :key="todo.id" :class="{ done: todo.done }" @click="toggleDone(todo)">
        {{ todo.text }}
      </li>
    </ul>
    <p v-if="todos.every(t => t.done)">🎉 Todas as tarefas concluídas!</p>
  </div>
</template>

<style scoped>
.todo-list-container {
  padding: 20px;
}
ul {
  list-style: none;
  padding: 0;
}
li {
  padding: 10px;
  border-bottom: 1px solid #eee;
  cursor: pointer;
}
.done {
  text-decoration: line-through;
  color: #888;
}
</style>