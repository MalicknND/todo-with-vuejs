<template>
  <!-- Formulaire d'ajout de tâche -->
  <form @submit.prevent="addTodo">
    <fieldset role="group">
      <input type="text" placeholder="Ajouter une tâche" v-model="newTodo" />
      <button :disabled="newTodo.length === 0">Ajouter</button>
    </fieldset>
  </form>

  <!-- Message si aucune tâche -->
  <div v-if="todos.length === 0">
    <p>Aucune tâche à faire pour le moment 😏</p>
  </div>

  <!-- Liste des tâches -->
  <div v-else>
    <ul>
      <li v-for="todo in sortedTodos()" :key="todo.id">
        <label :for="todo.id">
          <input type="checkbox" v-model="todo.completed" />
          <span :class="{ completed: todo.completed }">
            {{ todo.title }}
          </span>
        </label>
      </li>
    </ul>

    <!-- Option pour masquer les tâches complétées -->
    <label>
      <input type="checkbox" v-model="hideCompleted" />
      Masquer les tâches complétées
    </label>
  </div>
</template>

<script setup>
import { ref } from "vue";

// ✅ Champ texte lié à l’input
const newTodo = ref("");

// ✅ Checkbox pour masquer les tâches complétées
const hideCompleted = ref(false);

// ✅ Liste des tâches initiales
const todos = ref([
  {
    id: 1,
    title: "Faire ma déclaration fiscale",
    completed: false,
    date: new Date().toISOString().split("T")[0], // format : YYYY-MM-DD
  },
  {
    id: 2,
    title: "Faire mes devoirs",
    completed: true,
    date: new Date().toISOString().split("T")[0],
  },
]);

// ✅ Fonction pour ajouter une nouvelle tâche
const addTodo = () => {
  if (newTodo.value.trim() === "") return;

  todos.value.push({
    id: todos.value.length + 1,
    title: newTodo.value.trim(),
    completed: false,
    date: new Date().toISOString().split("T")[0],
  });

  // Réinitialise le champ texte
  newTodo.value = "";
};

// ✅ Fonction pour trier et filtrer les tâches
const sortedTodos = () => {
  // Trie : tâches non complétées en premier
  const sorted = todos.value.toSorted((a, b) =>
    a.completed > b.completed ? 1 : -1
  );

  // Filtre si l'option "masquer les tâches complétées" est activée
  return hideCompleted.value
    ? sorted.filter((todo) => !todo.completed)
    : sorted;
};
</script>

<style scoped>
/* ✅ Style pour les tâches complétées */
.completed {
  text-decoration: line-through;
  color: gray;
}
</style>
