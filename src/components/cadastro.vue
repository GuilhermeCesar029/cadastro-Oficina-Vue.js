<!--<template>
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
</template>-->

<template>
  <v-row justify="center">
    <v-col cols="12" sm="10" md="8" lg="6">
      <v-form ref="form"
        v-model="valid"
        lazy-validation>
        <v-card ref="form">
          <v-card-text>
            <v-text-field
              v-model="nomeField"
              box
              color="deep-purple"
              label="Nome"
              placeholder="Nome"
              required
            ></v-text-field>
            <v-text-field
              v-model="sobreNomeField"
              box
              color="deep-purple"
              label="sobrenome"
              placeholder="Sobrenome"
              required
            ></v-text-field>
            <v-text-field
              v-model="emailField"
              box
              color="deep-purple"
              label="email"
              placeholder="sistema@gmail.com"
              required
            ></v-text-field>
            <v-text-field
              v-model="cpfField"
              box
              color="deep-purple"
              label="CPF"
              placeholder="000.000.000-00"
              mask="###.###.###-##"
              required
            ></v-text-field>
            <v-text-field
              v-model="placaField"
              box
              color="deep-purple"
              label="Placa do Veiculo"
              placeholder="AAA-0000"
              mask="AAA-###"
              required
            ></v-text-field>
            <v-btn :disabled="!valid" color="success">cadastrar</v-btn>
          </v-card-text>          
        </v-card>
      </v-form>  
    </v-col>
  </v-row>
</template>

<script>

export default {
  data(){
     mask: '/^[a-z][0-9]+(-[a-z][0-9]+)*$/'
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

<!--
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
</style>-->
