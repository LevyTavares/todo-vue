<template>
  <ul class="task-list">
    <TaskItem
      v-for="(task, index) in tasks"
      :key="task.id" 
      :task="task"
      @remove="$emit('remove-task', index)"
    />
  </ul>
</template>

<script>
import TaskItem from './TaskItem.vue';

export default {
  components: {
    TaskItem
  },
  props: {
    tasks: { // Array de tarefas vindo do App.vue
      type: Array,
      default: () => []
    }
  },
  emits: ['remove-task']
}
</script>

<style scoped>
/* Estilização SCoped */
.task-list {
  list-style: none;
  padding: 0;
  margin-top: 20px;
}
</style>