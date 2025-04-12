<template>
  <form action="" @submit.prevent="addTodo">
    <fieldset role="group">
      <input type="text" placeholder="Ajouter une tâche" />
      <button>Ajouter</button>
    </fieldset>
  </form>
  <div v-if="todos.length === 0">
    <p>Aucune tâche à faire pour le moment 😏</p>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";

const todos = ref([]);
</script>

<style scoped>
.completed {
  text-decoration: line-through;
  color: gray;
}
</style>
