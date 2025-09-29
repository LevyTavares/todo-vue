<template>
  <li class="task-item">
    <span>{{ task.text }}</span>
    <button @click="$emit('remove')">Remover</button>
  </li>
</template>

<script>
export default {
  // Recebe a tarefa individual como uma propriedade (prop)
  props: {
    task: {
      type: Object,
      required: true
    }
  },
  emits: ['remove'] // Declara o evento que será emitido
}
</script>

<style scoped>
/* 4. ESTILIZAÇÃO - style scoped para isolar o CSS */
.task-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  border-bottom: 1px solid #eeeeee;
}

.task-item span {
  flex-grow: 1;
}

.task-item button {
  background-color: #dc3545;
  color: white;
  border: none;
  padding: 5px 10px;
  border-radius: 4px;
  cursor: pointer;
}
.task-item button:hover {
  background-color: #c82333;
}
</style>