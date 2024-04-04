<template>
  <!-- Propriedades computadas -->
  <div>Computed-Todo</div>

  {{ fullName }}

  <br />
  <br />
  <h2>Todas as Todos</h2>

  <div v-for="todo in todos" :key="todo.id">
    <input type="checkbox" v-model="todo.completed" />
    {{ todo.title }}
  </div>

  <h2>Todos não completadas</h2>

  <div v-for="todo in unCompletedTodo" :key="todo.id">
    {{ todo.title }}
  </div>

  <h2>Todos completadas</h2>

  <div v-for="todo in completedTodo" :key="todo.id">
    {{ todo.title }}
  </div>
</template>

<script>
export default {
  name: "Computed-Todo",
  data() {
    return {
      users: { first_name: "Isaac", last_name: "Newtown" },
      todos: [
        {
          userId: 1,
          id: 1,
          title: "delectus aut autem",
          completed: false,
        },
        {
          userId: 1,
          id: 2,
          title: "quis ut nam facilis et officia qui",
          completed: false,
        },
        {
          userId: 1,
          id: 3,
          title: "fugiat veniam minus",
          completed: false,
        },
        {
          userId: 1,
          id: 4,
          title: "et porro tempora",
          completed: true,
        },
        {
          userId: 1,
          id: 5,
          title:
            "laboriosam mollitia et enim quasi adipisci quia provident illum",
          completed: false,
        },
      ],
    };
  },
  computed: {
    fullName() {
      return `${this.users.first_name} ${this.users.last_name}`;
    },
    unCompletedTodo() {
      return this.todos.filter((td) => !td.completed);
    },
    completedTodo() {
      return this.todos.filter((td) => td.completed);
    },
  },
  methods: {},
};
</script>
