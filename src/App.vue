<template>
  <form action="" @submit.prevent="addTodo">
    <fieldset role="group">
      <input type="text" placeholder="Ajouter une tâche" v-model="newTodo" />
      <button :disabled="newTodo.length === 0">Ajouter</button>
    </fieldset>
  </form>
  <div v-if="todos.length === 0">
    <p>Aucune tâche à faire pour le moment 😏</p>
  </div>
  <div v-else>
    <ul>
      <li v-for="todo in sortedTodos()" :key="todo.id">
        <label :for="todo.id">
          <input type="checkbox" v-model="todo.completed" />
          <span :class="{ completed: todo.completed }">{{ todo.title }}</span>
        </label>
      </li>
    </ul>
    <label for="">
      <input type="checkbox" v-model="hideCompleted" />
      Masquer les tâches complétées
    </label>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";

const newTodo = ref("");
const hideCompleted = ref(false);
const todos = ref([
  {
    id: 1,
    title: "Faire ma déclaration fiscale",
    completed: false,
    date: new Date().toISOString().split("T")[0],
  },
  {
    id: 2,
    title: "Faire mes devoirs",
    completed: true,
    date: new Date().toISOString().split("T")[0],
  },
]);

const addTodo = () => {
  todos.value.push({
    id: todos.value.length + 1,
    title: newTodo.value,
    completed: false,
    date: new Date().toISOString().split("T")[0],
  });
  newTodo.value = "";
};

const sortedTodos = () => {
  const sortedTodo = todos.value.toSorted((a, b) =>
    a.completed > b.completed ? 1 : -1
  );
  if (hideCompleted.value === true) {
    return sortedTodo.filter((todo) => !todo.completed);
  }
  return sortedTodo;
};
</script>

<style scoped>
.completed {
  text-decoration: line-through;
  color: gray;
}
</style>
