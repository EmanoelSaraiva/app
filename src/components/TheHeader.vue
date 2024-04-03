<template>
  <div>
    <div>
      One-way data binding <br />
      Two-way data binding <br />
      v-model -> formulários
    </div>
  </div>
  <br />
  <div>
    <label>Nome</label> <br />
    <input type="text" v-model="todos.nome" /> <br />
    <p>Seu nome {{ todos.nome }}</p>
  </div>

  <div>
    <label>Cores</label> <br />
    <!-- Em caso de checkbox tenho a opção de true ou false para retornar condições binárias ou um array para multiplas escolhas -->
    <input type="checkbox" value="Azul" v-model="todos.colors" /> Azul
    <input type="checkbox" value="Vermelho" v-model="todos.colors" /> Vermelho
    <input type="checkbox" value="Roxo" v-model="todos.colors" /> Roxo <br />
    <p>Suas cores favoritas: {{ todos.colors }}</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      todos: {
        nome: "Teste",
        colors: [],
      },
    };
  },
};
</script>

<style>
header {
  background-color: #325;
  color: #fff;
}
</style>
