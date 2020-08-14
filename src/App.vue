<template>
  <div id="app">
    <h3>Cadastro de Clientes</h3>
    <input type="text" placeholder="nome" v-model="nomeField"><br>
    <input type="text" placeholder="sobrenome" v-model="sobreNomeField"><br>
    <input type="text" placeholder="email" v-model="emailField"><br>
    <input type="text" placeholder="###.###.###-##" v-model="cpfField"  v-mask="'###.###.#####'"><br>
    <input type="text" placeholder="AAA-###" v-model="placaField" v-mask="'AAA-###'"><br>
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

</style>
