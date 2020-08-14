<template>
  <div id="app">
    <h3>Cadastro de Clientes</h3>
    <form action="">
      <input type="text" placeholder="nome" v-model="nomeField" required><br>
      <input type="text" placeholder="sobrenome" v-model="sobreNomeField" required><br>
      <input type="email" placeholder="email" v-model="emailField" required><br>
      <input type="text" placeholder="###.###.###-##" v-model="cpfField"  v-mask="'###.###.###-##'" required><br>
      <input type="text" placeholder="AAA-####" v-model="placaField" v-mask="'AAA-####'" required><br>
      <button type="submit">cadastrar</button>
    </form>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      nomeField: "",
      sobreNomeField: "",
      emailField: "",
      cpfField: "",
      placaField: "",
    }
  },
  components: {
  
  }
  
}
</script>

<style>
  #app {
    text-align: center;
  }
</style>
