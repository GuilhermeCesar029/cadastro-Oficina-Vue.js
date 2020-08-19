<template>
  <v-app>
    <v-main>
      <h2 class="text-center">Cadastro de Clientes</h2>
      <cadastro/>
    </v-main>
  </v-app>
</template>

<script>
import cadastro from './components/cadastro';

export default {
  name: 'App',

  components: {
    cadastro,
  },

  data: () => ({
    //
  }),
};
</script>
