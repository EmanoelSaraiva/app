<template>
  <div>
    <form>
      <label>Nome</label><br />
      <input type="text" v-model="name" />
      <!-- Diretivas do Vue onde posso subistituir o v-on por @ e também usar o modificador .prevent() para evitar o reload da página na submissão do formulário -->
      <button @click.prevent="onClick(name)">Enviar</button>
    </form>
    <br />
    <!-- Outra forma de se fazer é com submit no form's, usando o .prevent() que é um modificador de ação-->
    <form @submit.prevent="onSubmit(name2)">
      <label>Nome</label><br />
      <input type="text" v-model="name2" />
      <button type="submit">Enviar</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      name: "",
      name2: "",
    };
  },
  methods: {
    onClick(name) {
      console.log("Hello World " + name);
    },
    onSubmit(name2) {
      console.log("Hello World " + name2);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
