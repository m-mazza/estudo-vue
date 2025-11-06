<script setup>
// Define o ano atual
const currentYear = new Date().getFullYear();
</script>

<template>
  <footer class="app-footer">
    <p>&copy; {{ currentYear }} Aplicação Todo. Desenvolvido com Vue.js.</p>
  </footer>
</template>

<style scoped>
.app-footer {
  background-color: #f4f4f4;
  color: #666;
  text-align: center;
  padding: 10px 0;
  border-top: 1px solid #ccc;
  font-size: 0.9em;
}
</style>