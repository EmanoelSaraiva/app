<template>
  <div>
    <form>
      <label>Nome</label><br />
      <input type="text" v-model="name" />
      <!-- Diretivas do Vue onde posso subistituir o v-on por @ e também usar o método .prevent() para evitar o reload da página na submissão do formulário -->
      <button @click.prevent="onClick(name)">Enviar</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      name: "",
    };
  },
  methods: {
    onClick(name) {
      console.log("Hello World " + name);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
