<template>
    <div>
        <form action="">
            <label for="">Nome: </label>
            <input type="text" placeholder="nome" v-model="nomeField" required><br>

            <label for="">sobrenome: </label>
            <input type="text" placeholder="sobrenome" v-model="sobreNomeField" required><br>

            <label for="">Email: </label>
            <input type="email" placeholder="email" v-model="emailField" required><br>

            <label for="">CPF:</label>
            <input type="text" placeholder="###.###.###-##" v-model="cpfField"  v-mask="'###.###.###-##'" required><br>
            
            <label for="">Placa do veiculo</label>
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
</style>
