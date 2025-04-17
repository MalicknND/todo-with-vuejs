<template>
  <div>
    <input type="checkbox" v-model="model" />
    {{ label }}
  </div>
</template>

<script setup>
const model = defineModel();
defineProps({
  label: String,
});
</script>

<style scoped></style>
