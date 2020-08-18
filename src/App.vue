<template>
  <div id="app">
    <h2>Cadastro de Clientes</h2>
    <cadastro/>
  </div>
</template>

<script>
  import cadastro from './components/cadastro'

  export default {
    name: 'App',
    components: {
      cadastro
    }
  }
</script>

<style scoped>
  h2{
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }
</style>