# 📝 Lista de Tarefas - Vue 3

Uma aplicação simples e funcional de lista de tarefas (To-Do List) desenvolvida com Vue 3 e Vite. Este projeto demonstra conceitos fundamentais do Vue.js, incluindo componentes, comunicação entre componentes, reatividade e gerenciamento de estado.

## ✨ Funcionalidades

- ✅ Adicionar novas tarefas
- 🗑️ Remover tarefas existentes
- 📱 Interface responsiva e intuitiva
- ⚡ Hot-reload durante o desenvolvimento
- 🎨 Estilização com CSS scoped

## 🛠️ Tecnologias Utilizadas

- **Vue 3** (^3.5.22) - Framework JavaScript progressivo
- **Vite** (^7.1.7) - Build tool rápida e moderna
- **JavaScript ES6+** - Linguagem de programação
- **CSS3** - Estilização dos componentes

## 📁 Estrutura do Projeto

```
src/
├── App.vue              # Componente principal da aplicação
├── main.js              # Ponto de entrada da aplicação
├── components/
│   ├── TaskList.vue     # Componente lista de tarefas
│   └── TaskItem.vue     # Componente item individual da tarefa
├── assets/
│   ├── base.css         # Estilos base
│   ├── main.css         # Estilos principais
│   └── logo.svg         # Logo do projeto
public/
└── favicon.ico          # Ícone da aplicação
```

## 🧩 Arquitetura dos Componentes

### App.vue

- Componente raiz da aplicação
- Gerencia o estado global das tarefas
- Contém métodos para adicionar e remover tarefas
- Passa dados para componentes filhos via props

### TaskList.vue

- Renderiza a lista de tarefas
- Recebe array de tarefas como prop
- Emite eventos para o componente pai

### TaskItem.vue

- Representa uma tarefa individual
- Recebe objeto de tarefa como prop
- Emite evento de remoção para o componente pai

## 💻 Configuração Recomendada do IDE

[VS Code](https://code.visualstudio.com/) + [Vue (Official)](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (desabilite o Vetur se estiver instalado).

## 🌐 Configuração Recomendada do Navegador

### Navegadores baseados em Chromium (Chrome, Edge, Brave, etc.):

- [Vue.js devtools](https://chromewebstore.google.com/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
- [Ativar Custom Object Formatter no Chrome DevTools](http://bit.ly/object-formatters)

### Firefox:

- [Vue.js devtools](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/)
- [Ativar Custom Object Formatter no Firefox DevTools](https://fxdx.dev/firefox-devtools-custom-object-formatters/)

## 🚀 Configuração do Projeto

### Instalação das Dependências

```sh
npm install
```

### Executar em Modo de Desenvolvimento

```sh
npm run dev
```

> A aplicação estará disponível em `http://localhost:5173`

### Compilar para Produção

```sh
npm run build
```

### Visualizar Build de Produção

```sh
npm run preview
```

## 📚 Conceitos Vue.js Demonstrados

### 1. **Componentes**

- Criação de componentes reutilizáveis
- Organização modular do código

### 2. **Props**

- Passagem de dados do componente pai para filho
- Validação de tipos de props

### 3. **Emits**

- Comunicação do componente filho para pai
- Declaração e emissão de eventos customizados

### 4. **Reatividade**

- Uso do sistema de reatividade do Vue
- Data binding com `v-model`

### 5. **Diretivas**

- `v-for` para renderização de listas
- `v-model` para binding bidirecional
- `@keyup.enter` para eventos de teclado

### 6. **Estilos Scoped**

- CSS isolado por componente
- Evita conflitos de estilo

## 🎯 Objetivos de Aprendizado

Este projeto é ideal para:

- Iniciantes em Vue.js que querem entender conceitos básicos
- Estudantes aprendendo sobre arquitetura de componentes
- Desenvolvedores explorando o ecossistema Vue 3 + Vite
- Demonstração de boas práticas em desenvolvimento frontend

## 🔧 Personalização

Para personalizar a configuração do Vite, consulte a [Referência de Configuração do Vite](https://vite.dev/config/).

## 📈 Possíveis Melhorias Futuras

- [ ] Marcar tarefas como concluídas
- [ ] Editar tarefas existentes
- [ ] Filtrar tarefas (todas, pendentes, concluídas)
- [ ] Persistência de dados (localStorage)
- [ ] Drag and drop para reordenar
- [ ] Temas (modo claro/escuro)
- [ ] Categorias de tarefas

---

**Desenvolvido como projeto educacional para aprendizado de Vue 3** 🎓
