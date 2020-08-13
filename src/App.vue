<template>
  <div id="app">
    <h3>Cadastro de Clientes</h3>
    <input type="text" placeholder="nome" v-model="nomeField"><br>
    <input type="text" placeholder="sobrenome" v-model="sobreNomeField"><br>
    <input type="text" placeholder="email" v-model="emailField"><br>
    <input type="number" placeholder="CPF" v-model="cpfField"><br>
    <input type="text" placeholder="placa do carro" v-model="placaField"><br>
    <button @click="cadastrarUsuario">Cadastrar</button>
    <hr>
                                      <!--key para identificar um cliente do outro-->
    <div v-for="cliente in clientes" :key="cliente.id">
      <Oficina :cliente="cliente"/>
    </div>
  </div>
</template>

<script>
  import Oficina from './components/Oficina'

export default {
  name: 'App',
  data(){
    return {
      nomeField: "",
      sobreNomeField: "",
      emailField: "",
      cpfField: "",
      placaField: "",
      clientes: [
        {
          id:1,
          nome: "Guilherme",
          sobrenome: "césar",
          email: "guilherme@gmail.com",
          cpf: 122222,
          placa: "ass22"
        }
      ]
    }
  },
  components: {
    Oficina
  },
  methods: {
    cadastrarUsuario: function(){
      this.clientes.push({
        nome: this.nomeField, 
        sobrenome: this.sobreNomeField, 
        email: this.emailField, 
        cpf: this.cpfField, 
        placa: this.placaField, 
        id: Date.now() //data atual

      })

      //limpar campos
      this.nomeField = "";
      this.sobreNomeField = "";
      this.emailField = "";
      this.cpfField = "";
      this.placaField = "";
    }
  }
}
</script>

<style>

</style>
