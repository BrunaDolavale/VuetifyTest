<template>
  <v-layout row wrap>
   <v-container grid-list-xl text-xs-center>
    <v-flex xs10 offset-xs1>
      <div id="listaUnidadesDeRede">
        <v-card-text><h2>Unidades de Rede</h2></v-card-text>
          <v-data-table
            :headers="headers"
            :items="items"
            hide-actions
            class="elevation-1"
          >
            <template slot="items" slot-scope="props">
              <td style="width: 60px"><input type="checkbox"></td>
              <td style="width: 60px">{{ props.item.name }}</td>
              <td class="text-xs-left">{{ props.item.path }}</td>
            </template>
          </v-data-table>
        </div>  
      </v-flex>
    </v-container>
  </v-layout>
</template>
<script>

export default {
  name: 'NcRedes',
  data: () => ({
    headers: [
      { text: '#' },
      { text: 'Letra' },
      { text: 'Caminho'  },
    ],
    items: [
      {
        value: false,
        name: 'Z',
        path: '\\\\fgvfsbi.fgv.br\\EPGE',
      },
      {
        value: false,
        name: 'W',
        path: '\\\\bo2002.fgv.br\\user\\bruna.dolavale',
      }
    ],
  }),
};
</script>