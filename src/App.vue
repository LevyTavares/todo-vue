<script>
import TaskList from './components/TaskList.vue';

export default {
  components: {
    TaskList
  },
  data() {
    return {
      // Estado para o texto da nova tarefa
      newTaskText: '', 
      // Array principal para armazenar as tarefas
      tasks: [
        { id: 1, text: 'Configurar o projeto Vue' },
        { id: 2, text: 'Criar componentes TaskList e TaskItem' }
      ],
      nextId: 3 // Contador simples para IDs
    };
  },
  methods: {
    addTask() {
      const text = this.newTaskText.trim();
      if (text) {
        // Adiciona a nova tarefa ao array
        this.tasks.push({
          id: this.nextId++,
          text: text
        });
        // Limpa o input
        this.newTaskText = '';
      }
    },
    removeTask(index) {
      // Remove a tarefa do array usando o índice
      this.tasks.splice(index, 1);
    }
  }
}
</script>

<template>
  <div id="app">
    <h1>Lista de Tarefas</h1>
    
    <div class="add-task">
      <input 
        type="text" 
        v-model="newTaskText" 
        placeholder="Adicionar nova tarefa..."
        @keyup.enter="addTask"
      >
      <button @click="addTask" :disabled="!newTaskText.trim()">Adicionar</button>
    </div>

    <TaskList :tasks="tasks" @remove-task="removeTask" />
  </div>
</template>


<style>
/* Estilização SCoped para o item individual */
.task-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px;
  margin-bottom: 8px;
  /* Estilização para contraste no Dark Mode */
  border: 1px solid #444444; 
  border-radius: 4px;
  background-color: #2a2a2a; /* Diferencia visualmente a tarefa */
}

.task-item span {
  flex-grow: 1;
  color: #e0e0e0; /* Texto da tarefa claro */
}

.task-item button {
  background-color: #ff4d4d;
  color: white;
  border: none;
  padding: 6px 12px;
  cursor: pointer;
  border-radius: 3px;
  margin-left: 10px;
  /* Ajuste no tamanho da fonte */
  font-size: 0.9rem;
}

#app {
  max-width: 600px;
  margin: 40px auto;
  padding: 20px;
  border-radius: 8px;
  background-color: #1e1e1e; /* Fundo escuro para o Dark Mode */
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5); /* Sombra mais suave */
  color: #f0f0f0; /* Texto claro para contraste */
}
h1 {
  text-align: center;
  margin-bottom: 20px;
  color: #ffffff; /* Título em branco para destaque */
}
.add-task {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}
.add-task input {
  flex-grow: 1;
  padding: 10px;
  border: 1px solid #444444; /* Borda mais escura */
  border-radius: 4px;
  margin-right: 10px;
  background-color: #2a2a2a; /* Fundo do input escuro */
  color: #e0e0e0; /* Texto claro */
}
.add-task input::placeholder {
  color: #888888; /* Placeholder em cinza claro */
}
.add-task button {
  padding: 10px 20px;
  background-color: #28a745; /* Verde para ação positiva */
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
.add-task button:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
</style>