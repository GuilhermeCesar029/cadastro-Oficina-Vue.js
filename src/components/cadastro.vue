<template>
    <div>
        <form id="cadastro" action="">
            <label for="">Nome: </label>
            <input type="text" placeholder="nome" v-model="nomeField" required><br>

            <label for="">Sobrenome:</label>
            <input type="text" placeholder="sobrenome" v-model="sobreNomeField" required><br>

            <label for="">Email: </label>
            <input type="email" placeholder="email" v-model="emailField" required><br>

            <label for="">CPF:</label>
            <input type="text" placeholder="###.###.###-##" v-model="cpfField"  v-mask="'###.###.###-##'" required><br>
            
            <label for="">Placa do veiculo: </label>
            <input type="text" placeholder="AAA-####" v-model="placaField" v-mask="'AAA-####'" required><br>
            <button type="submit">cadastrar</button>
        </form>
    </div>
</template>

<script>

export default {
  data(){
    return {
      nomeField: "",
      sobreNomeField: "",
      emailField: "",
      cpfField: "",
      placaField: "",
    }
  }  
}
</script>

<style>
  #app {
    text-align: center;
  }
  form#cadastro label{
    display: inline-block;
    width: 100px;
    text-align: right;
  }
  form#cadastro input {
      margin-top: 0.3em;
  }
  button{
      margin-top: 0.3em;
      font-size: 17px;
      border-radius: 15%;
      color: black;
  }
</style>
