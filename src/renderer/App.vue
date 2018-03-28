<template>
  <div id="app">
    <v-app>
      <v-content>
        <v-container>
          <nc-login></nc-login>
          <nc-redes></nc-redes>
          <!-- BOTAO OFICIAL
          <v-btn block append @click="submit":disabled="!valid" show = "true" v-model="teste" color="info">Conectar</v-btn>
          ### -->

<!--           BOTAO DE TESTE
          <v-btn block append @click="show = true" v-model="teste" color="info">TESTANDO</v-btn>  
          #### -->
        </v-container>
      </v-content>
    </v-app>
  </div>
</template>
<script>
import Vue from 'vue'
import Vuex from 'vuex'
import NcLogin from '@/components/NcLogin'
import NcRedes from '@/components/NcRedes'

export default {
  name: 'mapeia-unidade-de-rede',
  components: {
    NcLogin,
    NcRedes
  },
  data: () => ({
    show: false,
    title: 'Vuetify.js'
  })
}
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons');
/* Global CSS */
</style>
