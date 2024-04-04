<template>
  <div>Observadores</div>
  <input type="text" v-model="name" /> <br /><br />
  {{ name }}

  <br />
  <br />
  <br />

  <select v-model="pageCount">
    <option value="5">5</option>
    <option value="10">10</option>
    <option value="15">15</option>
  </select>

  {{ pageCount }}

  <br />
  <br />
  <br />

  <input type="text" v-model="users.first_name" />
  <input type="text" v-model="users.last_name" />
  <br /><br />
  {{ users.first_name }} {{ users.last_name }}
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "",
      pageCount: 5,
      users: {
        first_name: "",
        last_name: "",
      },
    };
  },
  watch: {
    name() {
      this.saveUserName();
    },
    pageCount() {
      this.changePage();
    },
    users: {
      handler() {
        console.log("User Alterado");
      },
      deep: true,
    },
  },
  computed: {},
  methods: {
    saveUserName() {
      console.log(this.name);
    },
    changePage() {
      console.log(this.pageCount);
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
</style>
