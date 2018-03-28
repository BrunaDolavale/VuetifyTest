<template>
  <v-layout row wrap>
   <v-container grid-list-xl text-xs-center>
    <v-flex xs10 offset-xs1>
      <v-card-text><h2>Login</h2></v-card-text>
    </v-flex>
    <v-flex xs10 offset-xs1>
      <v-form v-model="valid" ref="form" lazy-validation>
        <v-text-field id ="usuario" label="Usuário" v-model="usuario" :rules = "[ rules.required]" required></v-text-field>
        <v-text-field id = "senha" label="Senha" v-model="senha" type="password" :rules = "[rules.usuario_senha_errados, rules.required]" required></v-text-field>
        <v-btn block append @click="validate":disabled="!valid" color="info">Conectar</v-btn>
        <v-divider></v-divider>
      </v-form>
    </v-flex>
  </v-container>
</v-layout>
</template>
<script>


export default {
  name: 'NcLogin',
  data: () => ({
    alert: true,
    valid: false,
    senha: '',
    usuario: '',
    rules: {
      required: (value) => !!value || 'Campo Obrigatório',
      usuario_senha_errados: (value) => {
        return true;
      }
    }
  }),
  methods: {
    validate: function (event) {
      console.log(this.rules['usuario_senha_errados']);
    }
  }
};


   // export default {
   //  methods: {
   //    test: function() {
   //    alert('test fuction called');
   //   }
   //  }

   </script>
